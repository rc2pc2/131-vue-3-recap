<script>
import TodoListElement from './TodoListElement.vue';

export default {
    name: "TodoList",
    data() {
        return {
            todoElements : [
                {
                    id : 1,
                    label: "Fare la SPesa",
                    done : false,
                    removed : false,
                }, 
                {
                    id : 1,
                    label: "Comprare il lanciafiamme",
                    done : false,
                    removed : false,
                }, 
                {
                    id : 1,
                    label: "Aggiornare a WINDOWS tranquillo",
                    done : true,
                    removed : false,
                }, 
                {
                    id : 1,
                    label: "Acquistare un PALLOncinO banale",
                    done : false,
                    removed : false,
                }, 
                {
                    id : 1,
                    label: "Andare a SVILuppare Un pROgetto",
                    done : false,
                    removed : true,
                }, 
                {
                    id : 1,
                    label: "ParlARe con il pm",
                    done : false,
                    removed : false,
                }, 
                {
                    id : 1,
                    label: "Organizzarmi con i COLLEGHI e le colleghe",
                    done : true,
                    removed : false,
                }, 
            ]
        }
    },
    components:{
        TodoListElement
    },
    computed:{
        activeTodoElement(){
            return this.todoElements.filter((element) => element.removed === false);
        }
    }
}
</script>

<template>
    <h3>Todolist</h3>
    <ul>
        <TodoListElement v-for="todoElement in activeTodoElement" :todo="todoElement"/>
    </ul>
</template>

<style scoped>
    ul{
        text-align: left;
    }
</style>