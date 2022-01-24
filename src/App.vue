<template>
  <div id="app">
    <myEchart :options="options"></myEchart>
  </div>
</template>

<script>
import myEchart from './components/myEchart.vue'
import options from './option'
export default {
  name: 'App',
  components: {
    myEchart
  },
  data() {
    return {
      options:options
    }
  },
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
