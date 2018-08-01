/* eslint-disable */
<template>
  <div id="app">
    <img src="./assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js Counter App" />
    <p>{{count}}</p>
    <button @click="increment">↑</button>
    <button @click="decrement">↓</button>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import store from './store'

export default {
  name: 'app',
  components: {
    HelloWorld
  },
  computed: {
    count () {
      return store.state.count
    }
  },
  methods: {
    increment () {
      store.commit('increment')
    },
    decrement () {
      store.commit('decrement')
    }
  }
}
</script>

<style>
#app {
	font-family: "Avenir", Helvetica, Arial, sans-serif;
	-webkit-font-smoothing: antialiased;
	-moz-osx-font-smoothing: grayscale;
	text-align: center;
	color: #2c3e50;
	margin-top: 60px;
}
</style>
