<template>
  <div id="app">
      <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.0.2/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-EVSTQN3/azprG1Anm3QDgpJLIm9Nao0Yz1ztcQTwFspd3yD65VohhpuuCOmLASjC" crossorigin="anonymous">
  <div class="card" style="width: 18rem;">
  <div class="card-body">
    <p class="card-text">{{data.setup}}</p>
    <p class="card-text">{{data.punchline}}</p>
    <button class="btn btn-lg btn-primary btn btn-dark" @click.prevent="getJoke">Get Joke</button>
  </div>
</div>
  </div>
</template>
<script>
export default {
  name: "GetJokes",
  data() {
    return {
      data: {}
    }
  },
  methods: {
    async getJoke(){
      const res = await fetch('https://official-joke-api.appspot.com/random_joke');
      const data = await res.json();
      this.data = data;
      console.log("joke sent")
    }
  },
};
</script>
<style scoped>
#app {
    font-family: monospace;
    font-size: 30px;
    max-width: 400px;
    margin: auto;
    height: 85vh;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
}
</style>