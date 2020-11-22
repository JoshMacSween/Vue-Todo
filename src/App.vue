<template>
  <div id="app">
    <todos :todos="todos" />
    <add-todo v-on:add-todo="addTodo" />
  </div>
</template>

<script>
import AddTodo from './components/AddTodo.vue'
import Todos from './components/Todos.vue'
export default {
  components: { Todos, AddTodo },
  name: 'App',
  data() {
    return {
      todos: [
        {
          id: 1,
          title: 'Go workout',
          completed: false,
        },
        {
          id: 2,
          title: 'Do laundry',
          completed: false,
        },
        {
          id: 3,
          title: 'Cook food',
          completed: false,
        },
        {
          id: 4,
          title: 'Clean up room',
          completed: false,
        },
        {
          i: 5,
          title: 'Finish work',
          completed: false,
        },
      ],
    }
  },
  methods: {
    addTodo(newTodoObj) {
      this.todos = [...this.todos, newTodoObj]
    },
  },
}
</script>

<style>
  p {
    font-family: Arial, Helvetica, sans-serif;
  }
  h1, h2, h3, h4, h5 {
    font-family: Georgia, 'Times New Roman', Times, serif;
  }
</style>
