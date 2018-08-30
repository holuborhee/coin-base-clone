<template>
  <div id="app">
    <Login />
  </div>
</template>

<script>
import Login from './components/PageLogin.vue'

export default {
  name: 'app',
  components: {
    Login
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #333333;
  font-size: small;
}
</style>
