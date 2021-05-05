<template>
  <v-app>
    <v-app-bar
      app
      color="primary"
      dark
    >
      <v-app-bar-nav-icon @click="toggleSideMenu"></v-app-bar-nav-icon>
      <v-toolbar-title>アドレス帳</v-toolbar-title>
      <v-spacer></v-spacer>
    </v-app-bar>
    <SideNav/>

    <v-main>
      <router-view/>
    </v-main>
  </v-app>
</template>

<script>
import { mapActions } from 'vuex'
import SideNav from './components/SideNav'

export default {
  name: 'App',
  components: {
    SideNav
  },
  data: () => ({
    //
  }),
  methods: {
    ...mapActions(['toggleSideMenu'])
  }
};
</script>
