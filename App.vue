<template>
  <view class="container">
    <todo-item
      class="text-container"
      v-for="todo in todos"
      :key="todo.text"
      :item="todo"
    />
  </view>
</template>
 <script>
import TodoItem from "./todoItem";

export default {
  components: {TodoItem},
   data: function(){
     return{
       todos: [
         { id:1,text: "Learn JavaScript", status:true},
         { id:2,text: "Lean Vue", status:true},
         { id:3,text: "Build Something Awesome", status:true}
       ]
     }
   },
   methods: {

   },
 }
 </script>
<style>
.container {
  background-color: white;
  align-items: center;
  justify-content: center;
  flex: 1;
}
.text-color-primary {
  color: blue;
}
</style>
