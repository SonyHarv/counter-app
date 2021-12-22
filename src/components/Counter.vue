<template>
  <div>
    <h1>Hola Mundo desde Counter!!!</h1>
    <p>{{ counter }} <sup>2</sup> = {{ squareCounter }}</p>
  </div>
</template>
<script>
// import Counter from "@/components/Counter.vue";

export default {
  name: "Counter",
  data() {
    return {
      counter: 5,
    };
  },
  methods: {
    getSquareValue() {
      // console.log("getSquareValue");
      return this.counter * this.counter;
    },
  },
  computed: {
    squareCounter() {
      // console.log("computed squareCounter");
      return this.counter * this.counter;
    },
  },
};
</script>
<style>
h1 {
  color: green;
}
</style>
