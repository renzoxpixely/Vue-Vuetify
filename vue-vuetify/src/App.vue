<template>
  
  <v-app>

    <NavbarComponent></NavbarComponent>
    <v-content>
      <router-view/>
    </v-content>
    
  </v-app>

</template>

<script>
//import HelloWorld from "./components/HelloWorld";
import NavbarComponent from "./components/Navbar";

export default {
  components: {NavbarComponent},
  name: "App",
  data(){
    return {
      appTitle: 'Awesome App',
      sidebar: false,
      menuItems: [
          { title: 'Login', path: '/', icon: 'home' },
          { title: 'About', path: '/about', icon: 'face' },
          { title: 'Home', path: '/home', icon: 'lock_open' }
     ]
    }
  },
};
</script>
<style>

</style>
