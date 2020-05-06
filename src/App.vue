<template>
  <v-app>
      <v-app-bar
      app
      color="indigo darken-2"
      dark
      dense
    >
      <v-app-bar-nav-icon v-if="$vuetify.breakpoint.xsOnly"></v-app-bar-nav-icon>
      <v-img v-else src="./assets/avatar-icon.jpg" height="5vh" max-width="10vw" contain></v-img>

      <v-spacer v-if="!$vuetify.breakpoint.xsOnly"></v-spacer>

      <v-toolbar-title>Home</v-toolbar-title>

      <v-spacer></v-spacer>

      <v-btn icon>
        <v-icon>mdi-magnify</v-icon>
      </v-btn>

      <v-btn icon>
        <v-icon>mdi-heart</v-icon>
      </v-btn>

      <v-btn icon>
        <v-icon>mdi-dots-vertical</v-icon>
      </v-btn>
    </v-app-bar>

    <v-content>
      <router-view/>
    </v-content>
  </v-app>
</template>

<script>

export default {
  name: 'App',

  data: () => ({
    //
  }),
};
</script>
