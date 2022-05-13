<template>
  <h1>This is Homepage</h1>
</template>

<script>
export default {
  name: "HomeView",
  mounted() {
    let user = localStorage.getItem("users-info");
    if (!user) {
      this.$router.push({
        name: "SignUp",
      });
    }
  },
};
</script>

<style>
</style>