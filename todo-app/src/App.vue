<template>
  <div>
    <img src="./assets/logo.png">
    <todo-list v-bind:todos="todos"></todo-list>
  </div>
</template>


<script>
import TodoList from './components/TodoList';

export default {
  name: 'App',
  components: {
    TodoList,
  },

  data() {
    return {
      todos: [{
        id: 0,
        title: 'Todo A',
        project: 'Project A',
        isDone: false,
      }, {
        id: 1,
        title: 'Todo B',
        project: 'Project B',
        isDone: true,
      }, {
        id: 2,
        title: 'Todo C',
        project: 'Project C',
        isDone: false,
      }, {
        id: 3,
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
