<template>
  <div class="sign-up">
    <img src="../assets/logo.png" alt="" />
    <h1 class="sign-up-title">Sign Up</h1>
    <div class="sign-up-input">
      <input v-model="name" placeholder="Your Name" />
      <input v-model="email" type="email" placeholder="Your Email" />
      <input v-model="password" type="password" placeholder="Your Password" />
      <button @click="signUpBtnClick" class="submit-btn">Sign Up</button>
    </div>
  </div>
</template>


<script>
import axios from "axios";
export default {
  name: "SignUp",
  data() {
    return {
      name: "",
      email: "",
      password: "",
    };
  },
  methods: {
    async signUpBtnClick() {
      let email = this.email;
      let name = this.name;
      let password = this.password;

      let result = await axios.post("http://localhost:3000/users", {
        name: name,
        email: email,
        password: password,
      });
      if (result.status == 201) {
        console.log(result);
        localStorage.setItem("users-info", JSON.stringify(result.data));
      }
    },
  },
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