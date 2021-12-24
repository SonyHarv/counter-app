<script>
import Counter from "./components/Counter.vue";
export default {
  name: "App",
  components: {
    Counter,
  },
};
</script>

<template>
  <img alt="Vue logo" src="./assets/logo.png" />
  <h1>Counter</h1>
  <Counter title="Entraron"></Counter>
  <Counter :start="1"></Counter>
</template>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
