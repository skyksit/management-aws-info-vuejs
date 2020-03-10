<template>
  <div id="app" class="container">
    <b-container class="main" fluid>
      <v-menu />
      <router-view />
      <v-footer />
    </b-container>
  </div>
</template>

<script>
import Vue from "vue";
import Menu from "@/components/Menu";
import Footer from "@/components/Footer";

Vue.component("v-menu", Menu);
Vue.component("v-footer", Footer);

export default {
  name: "app",
  components: {},
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
