<template>
  <div>
    <!-- use reduce() instead?-->
    <p>Completed Tasks: {{todos.filter(todo => {return todo.isDone === true}).length}}</p>
    <p>Pending Tasks: {{todos.filter(todo => {return todo.isDone === false}).length}}</p>

    <!--perhaps instead use something like...
      <my-comp v-for="(item, index) in items" v-bind:item="item" v-bind:index="index"> </my-comp>
      -->
    <todo v-on:delete-todo="deleteTodo" v-for="todo in todos" :key="todo.id" v-bind:todo="todo"></todo>
  </div>
</template>

<script type="text/javascript">

import Todo from './Todo';

export default {
  props: ['todos'],
  components: {
    Todo,
  },
  methods: {
    deleteTodo(todo) {
      const todoIndex = this.todos.indexOf(todo);
      this.todos.splice(todoIndex, 1);
    },
  },
};

</script>

<style>

</style>

