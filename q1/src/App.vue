<template>
  <div id="app">
    <HelloWorld/>
    <bod/>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld'
import bod from './components/bod'

export default {
  name: 'App',
  components: {
    HelloWorld,
    bod
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
