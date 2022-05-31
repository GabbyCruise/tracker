<template>
  <div class="hello">
    {{ name }}

    <!-- {{ btnState ? 'the button is disabled' : 'The button is active' }} -->
    <!-- <button v-on:click="changeName" v-bind:disabled="btnState"> Change Name </button> -->

    <div class="holder">
      <ul>
        <li v-for="(data, index) in todo" :key='index'>{{ index }}. {{ data.action }}</li>
      </ul>
    </div>

  </div>
</template>

<script>
  export default {
    name: 'todo-list',
    data(){
      return {

        todo: [
          {'action': 'Watch vue tutorial'}, 
          {'action':'Follow tutorial coding samples'}
        ]
      }
    }
  }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  h3 {
    margin: 40px 0 0;
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
