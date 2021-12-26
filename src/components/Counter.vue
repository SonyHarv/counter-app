<template>
  <div>
    <h2>{{ customTitle }}</h2>
    <p>{{ counter }} <sup>2</sup> = {{ squareCounter }}</p>
  </div>
  <div>
    <button @click="incrementValue">+1</button>
    <button @click="decrementValue">-1</button>
  </div>
</template>
<script>
// import Counter from "@/components/Counter.vue";

export default {
  name: "Counter",

  props: {
    title: String,
    start: {
      type: Number,
      default: 15,
      validator(value) {
        return value >= 0;
      },
    },
  },
  data() {
    return {
      counter: this.start,
    };
  },
  methods: {
    getSquareValue() {
      // console.log("getSquareValue");
      return this.counter * this.counter;
    },
    incrementValue() {
      // console.log(this.incrementValue);
      this.counter++;
    },
    decrementValue() {
      this.counter--;
    },
  },
  computed: {
    squareCounter() {
      // console.log("computed squareCounter");
      return this.counter * this.counter;
    },
    customTitle() {
      // return this.title ? this.title : "Counter";
      return this.title || "Counter";
    },
  },
};
</script>

<style>
h1 {
  color: green;
}
button {
  color: white;
  padding-inline: 0.8rem;
  padding-block: 0.3rem;
  margin-inline-end: 0.7rem;
  border-radius: 5px;
  cursor: pointer;
  border: none;
  background: #4f9a6f;
  transition: 0.4s ease-in-out;
}
button:hover {
  background: #53b47d;
  transition: 0.4s ease-in-out;
}
</style>
