<template>
  <div id="app">
    <Horas/>
  </div>
</template>

<script>
import Horas from './components/Horas.vue'

export default {
  name: 'app',
  components: {
    Horas
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
