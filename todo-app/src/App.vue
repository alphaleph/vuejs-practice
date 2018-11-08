<template>
  <div>
    <img src="./assets/logo.png">
    <todo-list v-bind="todos"></todo-list>
  </div>
</template>


<script>
import TodoList from './components/TodoList';
//const uniqid = require('uniqid');

export default {
  name: 'App',
  components: {
    TodoList,
  },

  data() {
    return {
      todos: [{
        id: 0, //uniqid(),
        title: 'Todo A',
        project: 'Project A',
        isDone: false,
      }, {
        id: 1, //uniqid(),
        title: 'Todo B',
        project: 'Project B',
        isDone: true,
      }, {
        id: 2, //uniqid(),
        title: 'Todo C',
        project: 'Project C',
        isDone: false,
      }, {
        id: 3, //uniqid(),
        title: 'Todo C',
        project: 'Project C',
        isDone: false,
      }],
    };
  },
};
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
