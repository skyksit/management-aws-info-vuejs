<template>
  <b-navbar toggleable="md" type="dark">
    <b-navbar-toggle target="nav_collapse" />
    <b-navbar-brand to="/">AWS Console</b-navbar-brand>
    <b-navbar-nav>
      <b-nav-item to="/dashboard">Dashboard</b-nav-item>
      <b-nav-item to="/users">Users</b-nav-item>
    </b-navbar-nav>
    <b-navbar-nav class="ml-auto">
      <b-nav-item class="nav-btn" to="/login"
        ><span class="nav-username">Sign In</span></b-nav-item
      >
    </b-navbar-nav>
  </b-navbar>
</template>

<script>
export default {};
</script>

<style scoped>
.navbar {
  background-color: #563d7c;
}
.navbar-nav .nav-link {
  color: #cbbde2;
}
.nav-username {
  padding-left: 0.5em;
  padding-right: 0.5em;
}
</style>
