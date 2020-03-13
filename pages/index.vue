<template>
  <v-container>
    <v-row class="text-center">
      <v-col cols="12">
        <h1>Who am I?</h1>
      </v-col>
      <v-col cols="12">
        <v-avatar size="200">
          <v-img :src="require('@/assets/me.jpg')"></v-img>
        </v-avatar>
        <h2>Craig Peckett</h2>
        <v-card-text>
          Hello there, my name is Craig and I am a full stack web developer based in Sydney.
          I love building web applications from start to finish primarily focusing on simplicity and efficiency.
        </v-card-text>
        <v-btn class="primary" block>Contact Me</v-btn>
      </v-col>
    </v-row>
    <v-row class="text-center">
      <v-col cols="12">
        <h1>What can I do?</h1>
      </v-col>
      <v-col v-for="item in what" :key="item.title" cols="12">
        <v-icon size="100" color="primary">{{ item.icon }}</v-icon>
        <h2 class="subheader d-block">{{ item.title }}</h2>
        <v-card-text>{{ item.text }}</v-card-text>
      </v-col>
    </v-row>
    <v-row>
      <v-col cols="12">
        <h1 class="text-center">How can I do it?</h1>
        <v-list>
          <v-list-item v-for="item in how" :key="item.title" @click>
            <v-list-item-icon>
              <v-icon :color="item.colour">{{ item.icon }}</v-icon>
            </v-list-item-icon>

            <v-list-item-content>
              <v-list-item-title v-text="item.title"></v-list-item-title>
              <v-list-item-subtitle v-text="item.subtitle"></v-list-item-subtitle>
            </v-list-item-content>
          </v-list-item>
        </v-list>
        <!-- <h1>How can I do it?</h1>
        <v-card-text>
          I like to build my applications using the Vue CLI for the front end then Node JS and Express to set up the back end.
          When it comes to styling I have fallen in love with the material design component framework Vuetify but also have experience using Bootstrap and Bulma.
          
        </v-card-text>
      </v-col>
      <v-col v-for="item in how" :key="item.title" cols="12">
        <v-avatar tile size="150">
          <img :src="item.image" width="150" />
        </v-avatar>
        <v-btn
          class="mt-2"
          :style="{background: item.colour}"
          block
          :href="item.href"
        >{{ item.title }}</v-btn>-->
      </v-col>
    </v-row>
  </v-container>
</template>
<script>
export default {
  data() {
    return {
      what: [
        {
          icon: "mdi-tablet-cellphone",
          title: "Build",
          text:
            "I can build fully responsive web applications that work across all electronic devices and internet browsers."
        },
        {
          icon: "mdi-pencil",
          title: "Design",
          text:
            "I can design fast, simple websites that strengthens your company’s brand whilst presenting the ultimate user experience."
        },
        {
          icon: "mdi-account-check",
          title: "Gurantee",
          text:
            "I can gurantee a service of high quality and performance to gain 100% customer satisfaction or money back assured."
        }
      ],
      how: [
        {
          image: require("@/assets/vue.svg"),
          icon: "mdi-vuejs",
          title: "Vue JS",
          subtitle: "Javascript Framework",
          text:
            "I love to build the front end of my web appications using the progressive javascript framework Vue JS.",
          href: "https://vuejs.org/",
          colour: "#41b883"
        },
        {
          image: require("@/assets/vuetify.svg"),
          icon: "mdi-vuetify",
          title: "Vuetify",
          subtitle: "Vue UI Library",
          text:
            "When it comes to styling I have found nothing that compares to the material design component framework Vuetify.",
          href: "https://vuetifyjs.com/en/",
          colour: "#1f96f2"
        },
        {
          image: require("@/assets/node.svg"),
          icon: "mdi-nodejs",
          title: "Node JS",
          subtitle: "JavaScript Runtime",
          text:
            "When writing the back end of my applications I like to use the asynchronous event driven Javascript runtime Node JS.",
          href: "https://nodejs.org/en/",
          colour: "#3c873b"
        },
        {
          image: require("@/assets/firebase.svg"),
          icon: "mdi-firebase",
          title: "Firebase",
          subtitle: "Application Platform",
          text:
            "When writing the back end of my applications I like to use the asynchronous event driven Javascript runtime Node JS.",
          href: "https://firebase.google.com/",
          colour: "#f37f0a"
        },
        {
          image: require("@/assets/mongo.svg"),
          icon: "mdi-leaf",
          title: "Mongo DB",
          subtitle: "Document Database",
          text:
            "When writing the back end of my applications I like to use the asynchronous event driven Javascript runtime Node JS.",
          href: "https://firebase.google.com/",
          colour: "#3c873b"
        },
        {
          image: require("@/assets/nuxt.svg"),
          icon: "mdi-nuxt",
          title: "Nuxt JS",
          subtitle: "Vue JS Framework",
          text:
            "When writing the back end of my applications I like to use the asynchronous event driven Javascript runtime Node JS.",
          href: "https://firebase.google.com/",
          colour: "#41b883"
        }
      ]
    };
  }
};
</script>
