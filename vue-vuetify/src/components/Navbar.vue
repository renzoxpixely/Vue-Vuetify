<template>
<v-navigation-drawer v-model="sidebar" app>
  <v-list>
    <v-list-tile
      v-for="item in menuItems"
      :key="item.title"
      :to="item.path">
      <v-list-tile-action>
        <v-icon>{{ item.icon }}</v-icon>
      </v-list-tile-action>
      <v-list-tile-content>{{ item.title }}</v-list-tile-content>
    </v-list-tile>
  </v-list>
</v-navigation-drawer>

<v-toolbar app>
  <span class="hidden-sm-and-up">
    <v-toolbar-side-icon @click="sidebar = !sidebar">
    </v-toolbar-side-icon>
  </span>
  <v-toolbar-title>
    <router-link to="/">
      {{ appTitle }}
    </router-link>
  </v-toolbar-title>
  <v-spacer></v-spacer>
  <v-toolbar-items class="hidden-xs-only">
    <v-btn
      flat
      v-for="item in menuItems"
      :key="item.title"
      :to="item.path">
      <v-icon left dark>{{ item.icon }}</v-icon>
      {{ item.title }}
    </v-btn>
  </v-toolbar-items>
</v-toolbar>

</template>

<script>


export default {
  name: 'NavbarComponent',

  data(){
    return {
      appTitle: 'Awesome App',
      sidebar: false,
      menuItems: [
          { title: 'Login', path: '/', icon: 'home' },
          { title: 'About', path: '/about', icon: 'face' },
          { title: 'Home', path: '/home', icon: 'lock_open' }
     ]}}


}












</script>