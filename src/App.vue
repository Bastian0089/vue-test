<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <CrearLista></CrearLista>
</template>

<script>
import CrearLista from './components/CrearLista.vue'

export default {
  name: 'App',
  components: {
    CrearLista
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
