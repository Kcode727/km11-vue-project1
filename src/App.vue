<script setup>
import { ref } from "vue";

// Mock TODO data
const todos = ref([
  { description: "First todo", dueDate: "2024-10-30", completed: false },
  { description: "Second todo", dueDate: "2024-11-05", completed: true },
  { description: "Third todo", dueDate: "2024-12-01", completed: false },
]);
</script>

<template>
  <header>
    <nav>
      <ul>
        <li><strong>Todo Application</strong></li>
      </ul>
      <ul>
        <li><a href="/todos">List Todos</a></li>
        <li><a href="/todos/create">Add Todo</a></li>
      </ul>
    </nav>
  </header>

  <main class="container">
    <h1>TODO List</h1>
    <table>
      <thead>
        <tr>
          <th>Title</th>
          <th>Due Date</th>
          <th>Completed?</th>
        </tr>
      </thead>
      <tbody>
        <tr v-for="(todo, index) in todos" :key="index">
          <td>{{ todo.description }}</td>
          <td>{{ todo.dueDate }}</td>
          <td v-if="todo.completed">Yes</td>
          <td v-else>No</td>
        </tr>
      </tbody>
    </table>
  </main>
</template>

<style scoped>
</style>
