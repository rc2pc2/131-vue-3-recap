<script>
export default {
    data() {
      return {
        
      }
    },
    props: {
        todo: {
            required : true,
            type: Object,
        }
    },
    computed:{
        name(){
            return this.todo.label.charAt(0) + this.todo.label.substring(1).toLowerCase();
        },
        done(){
            if (this.todo.done === true ) return "done";
            return "";
        }
    },
    methods:{
        updateStatus(){
            this.todo.done = !this.todo.done;
        },
        deleteMe(){
            this.todo.removed = true;
        }
    }
}
</script>

<template>
    <li>
        <span @click="updateStatus" :class="done">{{ name }}</span> <span @click="deleteMe">CANCELLAMI</span>
    </li>
</template>

<style scoped>
    li>span.done{
        text-decoration: line-through;
    }
</style>