<template>
  <div id="app">
    <img
      class="background-image"
      alt="Forest Background"
      src="./assets/Coding-Challenge-Image.png"
    />
    <div class="sidebar" />
    <HelloWorld msg="Welcome to Your Vue.js App" />
    <div class="social-icons">
      <img alt="Facebook Logo" src="./assets/Facebook.svg" />
      <br/>
      <img alt="Facebook Logo" src="./assets/Instagram.svg" />
    </div>
  </div>
</template>

<script>
import HelloWorld from "./components/HelloWorld.vue";

export default {
  name: "app",
  components: {
    HelloWorld,
  },
};
</script>

<style>
html {
  width: 100%;
}
body {
  margin: 0px;
  padding: 0px;
  width: 100%;
}
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  position:relative;
  overflow: hidden;
}
.background-image {
  /* height: 100vh; */
  max-width: 100vw;
  min-width: 1200px;
  position: absolute;
  left: 0;
  top: 0;
  z-index: -5;
}
.sidebar {
  background-color: #611818;
  height: 100vh;
  width: 25vw;
}
.social-icons {
  position:absolute;
  right: 20px;
  bottom: 20px;
}
</style>
