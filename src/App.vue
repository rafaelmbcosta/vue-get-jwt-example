<template>
  <div id="app">
    <app-token> </app-token>
  </div>
</template>

<script>
import Token from './components/Token.vue'

export default {
  name: 'app',
  components: {
    'app-token': Token 
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
