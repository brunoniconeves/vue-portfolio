<template>
  <div id="app">
    <navBar/>   
    <router-view/>
  </div>
</template>

<style lang="scss">
@import './assets/styles/custom.scss';
@import '../node_modules/bootstrap/scss/bootstrap.scss';

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}


</style>

<script>
import navBar from "./components/navbar/navbar.vue"

export default {
  name: 'app',
  components: {
    navBar
  },
  data () {
    return {
      msg: 'Hello, World!'
    }
  }
}
</script>

