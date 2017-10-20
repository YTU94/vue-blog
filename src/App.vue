<template>
  <div id="app">
    <img src="./assets/logo.png">
    <button @click="test">test</button>
    <router-view/>
  </div>
</template>

<script>
import api from './api/api'
// import axios from 'axios'
export default {
  name: 'app',
  methods: {
    test () {
      // axios.get('/api').then(res => {
      //   console.log(res)
      // })
      api.test()
        .then(res => {
          console.log(res)
        })
        .catch(error => {
          console.log(error)
        })
    }
  }
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
