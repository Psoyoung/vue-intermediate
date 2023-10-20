<template>
  <div class="inputBox">
    <input type="text" v-model="newTodoItem">
    <button v-on:click="addTodo">add</button>
    <span class="addContainer">
      <i class="fa-solid fa-plus"></i>
    </span>
  </div>
</template>

<script>
export default {
  data: function(){
    return{
      newTodoItem: ""
    }
  },
  methods: {
    addTodo: function(){
      //console.log(this.newTodoItem);
      //저장하는 로직
      localStorage.setItem(this.newTodoItem, this.newTodoItem);
      this.clearInput();
    },
    clearInput: function() {
      this.newTodoItem = '';
    }
  }
}
</script>

<style>

</style>