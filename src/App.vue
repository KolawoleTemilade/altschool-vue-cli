<template>
  <ToDo/>
</template>

<script>
import ToDo from './components/ToDo.vue';

export default {
  name: 'App',
  components: {
    ToDo
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  text-align: center;
  margin-top: 60px;
  margin-left: 60px;
  margin-right: 60px;
  width: 50%;
  border: 2px solid brown;
  border-radius: 10px;
  background-color: rgba(220, 207, 190, 0.692);
}

form {
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: center;
  gap: 70px;
  padding: 30px;
}

input[type="text"] {
  padding: 10px;
  margin: 10px;
  border-radius: 5px;
  border: none;
  box-shadow: 0 0 5px rgba(0, 0, 0, 0.2);
}
.todo-input{
  font-size: 16px;
  padding: 10px;
}
button[type="submit"] {
  padding: 10px 50px;
  margin: 10px;
  border-radius: 5px;
  border: none;
  background-color: #4caf50;
  color: white;
  box-shadow: 0 0 5px rgba(0, 0, 0, 0.2);
  font-size: 15px;
}

button[type="submit"]:hover {
  background-color: #3e8e41;
}
 .todo-item {
  display: flex;
  justify-content: space-between;
  /* gap: 100px; */
   align-items: center;
  margin: 10px ;
  padding: 10px;
  border-radius: 5px;
  background-color: #f5f5f5;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.2);
}

.todo-item button {
  background-color: #f44336;
  color: white;
  border: none;
  border-radius: 5px;
  padding: 5px 10px;
  cursor: pointer;
}

.todo-item button:hover {
  background-color: #d32f2f;
} 
</style>
