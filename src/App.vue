<template>
  <div id="app">
    <UserLogin
      v-if="!isLoggedIn"
      @loginSuccess="isLoggedIn = true"
    /><!-- SOAL: tambahkan tag html sebelum directive berupa variabel yang di import di bagian script-->
    <UserDashboard
      v-else
      @logout="isLoggedIn = false"
    /><!-- SOAL: tambahkan tag html sebelum directive berupa variabel yang di import di bagian script-->
  </div>
</template>

<script>
import UserLogin from "./components/UserLogin.vue"; //SOAL: Definisikan variabel import
import UserDashboard from "./components/UserDashboard.vue"; //SOAL: Definisikan variabel import

export default {
  name: "App",
  components: {
    // SOAL: panggil components yang akan digunakan
    UserLogin,
    UserDashboard,
  },
  data() {
    return {
      isLoggedIn: false,
    };
  },
};
</script>

<style>
body {
  font-family: Arial, sans-serif;
}
</style>
