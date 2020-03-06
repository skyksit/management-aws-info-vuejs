<template>
  <div class="users">
    <h1>This is an Users page</h1>
    <Users />
  </div>
</template>

<script>
// @ is an alias to /src
import Users from "@/components/Users.vue";

export default {
  name: "userlist",
  components: {
    Users
  }
};
</script>
