<template>
  <div class="todo">
    <form @submit.prevent="add">
      <input v-model="todo" class="todo-input"/>
      <button type="submit">Add</button>

    </form>

    <div v-for="(todo, index) of todos" :key="todo.id" class="todo-item">
      {{ todo.todo }}
      <button @click="editTodo(index)">edit</button>
      <button @click="deleteTodo(index)">delete</button>
    </div>
  </div>
</template>
  
<script>
import { v4 as uuidv4 } from "uuid"

export default {
  data() {
    return {
      todo: "",
      todos: [],
    };
  },
  methods: {
    add() {
      const { todo } = this;
      if (todo.trim() === "") {
        // Alert when no input is entered
        alert("Please enter a task.");
        return false; // Prevent form submission
      }
      this.todos.push({
        id: uuidv4(),
        todo,
      });
      this.todo = ""; // Clear input field
    },
    deleteTodo(index) {
      this.todos.splice(index, 1);
    },
    editTodo(index) {
    const editedTodo = prompt("Edit the task:", this.todos[index].todo);
    if (editedTodo !== null) {
      this.todos[index].todo = editedTodo;
    }
  },
},
}
</script>