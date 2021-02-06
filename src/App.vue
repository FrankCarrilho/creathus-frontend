<template>
  <div id="app">
    <Estrutura />
  </div>
</template>

<script>
import Estrutura from './components/Estrutura.vue'

export default {
  name: 'App',
  components: {
    Estrutura
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

body {
    margin-bottom: 60px;
    background: #314755; /* fallback for old browsers */
    background: -webkit-linear-gradient(to right, #26a0da, #314755); /* Chrome 10-25, Safari 5.1-6 */
    background: linear-gradient(to right, #26a0da, #314755); /* W3C, IE 10+/ Edge, Firefox 16+, Chrome 26+, Opera 12+, Safari 7+ */
}

</style>
