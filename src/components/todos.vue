<template>
  <div class="hello">
    <div class="holder">

      <form @submit.prevent="addTodo">
        <input type="text" placeholder="Enter your todo item.." v-model="list" v-validate="'min:5'" name="list">
        {{list}} <!--shows the process of capturing user input-->
        <!-- <p class="alert" v-if="errors.has('list')">{{ errors.first('list') }}</p> -->
      </form>

      <ul>
        <li v-for="(data, index) in todos" :key='index'>{{ index }}. {{ data.action }}</li>
      </ul>

      <p>Your list of things to do today.</p>
    </div>

  </div>
</template>

<script>
  export default {
    name: 'todo-list',
    data(){
      return {
        list: '',

        todos: [
          {'action': 'Design a sketch for 360 UI app'}, 
          {'action':'Send sheet to the group'}
        ]
      }
    },

    methods: {
      addTodo(){
        this.todos.push({action: this.list})
        this.list = '';
      }
    }
  }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  .holder {
    background: #fff;
  }

  ul {
    margin: 0;
    padding: 0;
    list-style-type: none;
  }

  ul li {
    padding: 20px;
    font-size: 1.3em;
    background-color: #E0EDF4;
    border-left: 5px solid blue;
    margin-bottom: 2px;
    color: #3E5252;
  }

  p {
    text-align: center;
    padding: 30px 0;
    color: gray;
  }

  .container {
    box-shadow: 0px 0px 40px lightgray;
  }

  input {
    width: calc(100% - 40px);
    border: 0;
    padding: 20px;
    font-size: 1.3em;
    background-color: #323333;
    color: #687F7F;
  }
</style>
