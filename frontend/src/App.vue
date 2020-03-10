<template>
  <v-app>
    
    <v-app-bar
      app
      height=50
      color="grey darken-4"
    >
      <img class="mr-3" :src="require('@/assets/cv.png')" height="32"/>
      <v-toolbar-title>Coronavirus Prediction</v-toolbar-title>
    </v-app-bar>

    <v-content>
      <Home></Home>
    </v-content>

    <v-footer>
      <v-col
        class="text-center"
        cols="12"
      >
        <v-btn href="https://github.com/metesengul/coronavirus-prediction" class="grey--text" text small><v-icon left dark small>mdi-github</v-icon>Source Code</v-btn>
      </v-col>
    </v-footer>

  </v-app>
</template>

<script>
  import Home from '@/components/Home'

  export default {
    props: {
      source: String,
    },
    components: {
      Home
    },
    data: () => ({
    }),
    created () {
      this.$vuetify.theme.dark = true
    },
  }
</script>