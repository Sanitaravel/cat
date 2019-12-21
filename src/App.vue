<template>
  <div id="app">
    <Cats :fact = "factic"></Cats>
  </div>
</template>

<script>
import Cats from './components/Cats.vue'
import axios from 'axios'

export default {
  name: 'app',
  data(){
    return {
      factic: ''
    }
  },
  components: {
    Cats
  },
  mounted() {
    axios.get('http://188.225.47.187/api/cats/random-fact.php').then((response)=>{
      this.factic = response.data;
    },
    setInterval(() => axios.get('http://188.225.47.187/api/cats/random-fact.php').then((response)=>{
      this.factic = response.data;
    }), 10000))
  },
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
