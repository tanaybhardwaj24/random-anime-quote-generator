<template>
<div>
  <GetJokes />
</div>
</template>

<script>
import GetJokes from './components/GetJokes.vue'

export default {
  name: 'App',
  components: {
    GetJokes
  }
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
