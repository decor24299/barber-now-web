<template>
  <div id="app">
    <Navbar />
    <Main />
  </div>
</template>

<script>
import Navbar from "./components/Navbar.vue";
import Main from "./components/Main.vue";

export default {
  name: "App",
  components: {
    Navbar,
    Main,
  },
};
</script>

<style>
@import url("https://fonts.googleapis.com/css2?family=Inconsolata&display=swap");

*:focus {
  outline: none !important;
}

#app {
  font-family: "Inconsolata", sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
