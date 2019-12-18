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
  },
  created() {
    const locale = localStorage.getItem("locale");

    if (locale) {
      this.$i18n.locale = locale;
    } else if (navigator.language) {
      //this.$i18n.locale = navigator.language.substring(0, 2);
      this.$i18n.locale = navigator.language;
    }
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
.button {
  border: 1px solid black;
  padding: 8px;
  margin: 2px;
}
.button:hover {
  color: #2c3e50;
}
</style>
