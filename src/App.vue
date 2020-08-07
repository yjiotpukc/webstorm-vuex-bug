<template>
  <div id="app">
    <h1>Counter is {{ value }}</h1>
    <button @click="incrementCounter">Increment</button>
  </div>
</template>

<script>

import {mapMutations, mapState} from "vuex";

export default {
  name: 'App',
  computed: mapState("counter", ["value"]),
  methods: mapMutations({
    incrementCounter: "counter/increment"
  })
}
</script>

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
