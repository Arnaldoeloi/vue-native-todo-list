<template>
  <view class="container">
    <text>{{ newTodo }}</text>
    <text-input :on-add='_onPress'></text-input>
    <todo-item
      class="text-color-primary"
      v-for="todo in todos"
      :key="todo.text"
      :item="todo"
    />
  </view>
</template>
<script>
import TextInput from './todoInput';
import TodoItem from "./todoItem";

export default {
  components: {
    TodoItem,
    TextInput
  },
   data: function(){
     return{
       ids: 3,
       newTodo: '',
       todos: [
         { id:1,text: "Learn JavaScript", status:true},
         { id:2,text: "Lean Vue", status:true},
         { id:3,text: "Build Something Awesome", status:true}
       ]
     }
   },
   methods: {
       _onPress : function(req) {
          this.newTodo = req;
          this.ids+= 1;
          var todo = {id: this.ids, text: this.newTodo, status: false}
          this.addToList(todo)
       },
       addToList: function(newTodo){
         this.todos.push(newTodo);
       }   
   },
 }
 </script>
<style>
.container {
  background-color: #303030;
  align-items: center;
  justify-content: center;
  flex: 1;
}
.text-color-primary {
  color: #dfdfdf;
}
.main{
  flex:1;
  max-width: 400px;
  align-items: center;
}
</style>
