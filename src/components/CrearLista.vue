<template>
    <form @submit.prevent="addTodo">
      <input v-model="newTodo" required placeholder="new todo">
      <button>Add Todo</button>
    </form>
    <ul>
      <li v-for="todo in todos" :key="todo.id">
        {{ todo.text }}
        <button @click="removeTodo(todo)">X</button>
        <button @click="showRename()">Rename</button>
        <input v-model="renameTodo" hidden placeholder="new name">
        <button hidden>Change name</button>
      </li>
    </ul>
  </template>

<script setup>
import { ref } from 'vue'

let id = 0

const newTodo = ref('')
const todos = ref([])
const renameTodo = ref('')

function addTodo() {
  todos.value.push({ id: id++, text: newTodo.value })
  newTodo.value = ''
}

function removeTodo(todo) {
  todos.value = todos.value.filter((t) => t !== todo)
}
function showRename(){

}
</script>