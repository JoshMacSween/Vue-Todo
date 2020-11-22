<template>
  <div>
    <h2>My Todo List</h2>
    <ul>
      <li v-bind:key="todo.id" v-for="todo in todos">
        <todo v-bind:todo="todo" v-on:delete-todo="$emit('delete-todo', todo.id)"/>
      </li>
    </ul>
  </div>
</template>

<script>
import Todo from './Todo'
export default {
  name: 'Todos',
  components: {
    Todo,
  },
  props: ["todos"]
}
</script>

<style lang="scss" scoped></style>
