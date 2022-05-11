<template>
  <div class="sign-up">
    <img src="../assets/logo.png" alt="" />
    <h1 class="sign-up-title">Sign Up</h1>
    <div class="sign-up-input">
      <input type="text" placeholder="Your Name" />
      <input type="email" placeholder="Your Email" />
      <input type="password" placeholder="Your Password" />
      <button class="submit-btn">Submit</button>
    </div>
  </div>
</template>

<script>
export default {
  name: "SignUp",
};
</script>

<style scoped>
.sign-up {
  text-align: center;
}
.sign-up-input input {
  display: block;
  width: 300px;
  height: 5px;
  padding: 20px;
  margin-left: auto;
  margin-right: auto;
  margin-bottom: 15px;
}
.submit-btn {
  width: 350px;
  padding: 10px;
  background: blue;
  color: white;
  cursor: pointer;
}
</style>