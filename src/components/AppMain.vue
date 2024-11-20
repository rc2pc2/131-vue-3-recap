<script>
import TodoList from './TodoList.vue';

export default {
    data() {
      return {
        
      }
    },
    name: "AppMain",
    components:{
        TodoList
    }
}
</script>

<template>
    <h1>
        Todo List:
    </h1>
     
    <TodoList/>
</template>

<style scoped>
</style>