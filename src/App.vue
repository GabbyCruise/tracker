<template>
  <div id="app">
    <todos />
  </div>
</template>

<script>
  import todos from './components/todos.vue'
  export default {
    name: 'App',
    components: {
      todos
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
    font-size: 10px
  }
</style>
