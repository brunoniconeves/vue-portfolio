<template>
  <div id="app">
    <navbar/>
    <b-alert show dismissible> {{ msg }}! </b-alert>
    <b-list-group class="mt-5">
      <b-list-group-item v-for="item in items" v-bind:key="item.id">
      {{ item.message }}
      <b-badge>{{item.versions}}</b-badge>
      </b-list-group-item>
    </b-list-group>
    <div class="text-center m-5">
      <b-button variant="primary" size="sm" v-on:click="share_count += 1">
        Share on Twitter <b-badge variant="light">{{ share_count }}</b-badge>
      </b-button>
    </div>
  </div>
</template>

<script>
import navbar from './components/navbar/navbar.vue'

export default {
  name: 'app',
  components: {
    navbar
  },
  data () {
    return {
      msg: 'Isso é um teste',
      items: [
      { message: 'Nokia 8', versions: 5 },
      { message: 'OnePlus 5T' },
      { message: 'Samsung Galaxy S9' }
    ],
      share_count:0,
      teste: 'Teste'
    }
  }
}
</script>

<style lang="scss">
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

h1, h2 {
  font-weight: normal;
}

ul {
  list-style-type: none;
  padding: 0;
}

li {
  display: inline-block;
  margin: 0 10px;
}

a {
  color: #42b983;
}
</style>
