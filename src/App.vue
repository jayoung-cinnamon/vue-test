<template>
  <div id="app">
    <Header />
    <Main />
  </div>
</template>

<script>
import Main from "./components/Main.vue";
import Header from "./components/layout/Header.vue";
export default {
  name: "App",
  components: {
    Main,
    Header,
  },
};
</script>

<style scoped>
#app {
  width: 100%;
  display: flex;
  flex-direction: column;
  justify-content: center;
  background-color: white;
}
</style>
