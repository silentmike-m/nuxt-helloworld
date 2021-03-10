<template>
  <div>
    <Logo inputText="Login Page" />
    <form @submit.prevent="loginUser()">
      <input type="text" v-model="userName" />
      <input type="password" v-model="password" />
      <button type="submit">LOGIN</button>
    </form>
  </div>
</template>

<script lang="ts">
import Vue from "vue";
import Logo from "~/components/Logo.vue";

export default Vue.extend({
  components: {
    Logo,
  },
  data(): {
    userName: String;
    password: String;
  } {
    return {
      userName: "user name",
      password: "password",
    };
  },
  methods: {
    loginUser() {
      console.log(`userName: ${this.userName}`);
      console.log(`password: ${this.password}`);
    },
  },
});
</script>