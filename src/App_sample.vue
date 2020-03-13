<template>
  <div id="app" class="container">
    <b-container class="main" fluid>
      <v-menu />
      <v-footer />
    </b-container>
    <ul class="nav nav-tabs">
      <li v-bind:class="{ active: currentTab === 'SignUp' }">
        <a href="#" @click="switchTab('SignUp')">Sign Up</a>
      </li>
      <li v-bind:class="{ active: currentTab === 'Login' }">
        <a href="#" @click="switchTab('Login')">Login</a>
      </li>
    </ul>
    <Login v-if="currentTab === 'Login'"></Login>
    <b-navbar type="dark" variant="dark">
      <b-navbar-nav>
        <b-nav-item router-link to="/"
          ><a href="#" @click="switchTab('Home')">Home</a></b-nav-item
        >
        <b-nav-item router-link to="/users"
          ><a href="#" @click="switchTab('Users')">Users</a></b-nav-item
        >
        |
        <b-nav-item router-link to="/about"
          ><a href="#" @click="switchTab('About')">About</a></b-nav-item
        >
      </b-navbar-nav>
    </b-navbar>
    <router-view />
  </div>
</template>

<script>
import Vue from "vue";
import Login from "@/components/Login";
import Menu from "@/components/Menu";
import Footer from "@/components/Footer";

Vue.component("v-menu", Menu);
Vue.component("v-footer", Footer);

export default {
  name: "app",
  components: {
    Login
  },
  data: () => ({
    currentTab: "Home"
  }),
  methods: {
    switchTab(tab) {
      this.currentTab = tab;
    }
  }
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

.nav-tabs {
  margin-bottom: 25px;
}
</style>
