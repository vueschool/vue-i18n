<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png" />
    <HelloI18n />
  </div>
</template>

<script>
import HelloI18n from "./components/HelloI18n.vue";

export default {
  name: "app",
  components: {
    HelloI18n
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
.btn {
  border: 1px solid black;
  padding: 8px;
  margin: 2px;
}
.btn:hover {
  color: #2c3e50;
}
</style>
