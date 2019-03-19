<template>
    <div id="todos" class="container">
        <h1>Todo List</h1>
        
        <div class="todo-list">
            <input class="form-control" :value="newTodo" @change="getTodo" @keyup.enter="addTodo" placeholder="New Todo ...">
            <button class="btn btn-primary" @click="addTodo">Add</button>
        </div>
    </div>
</template>

<script>
    import api from '@/api'
    import { mapMutations } from 'vuex'
    
    export default{
        data() {
            return {
                todos: {}
            }
        },
        methods: {
            getTodo(e){
                this.$store.dispatch('getTodo', e.target.value)
            },
            addTodo(){
                this.$store.dispatch('addTodo')
                this.$store.dispatch('clearTodo')
            }
        },
        computed: {
            newTodo(){
                return this.$store.getters.newTodo
            }
        }
    }
</script>

<style>
    #todos{
        margin-top: 50px;
    }
    .todo-list {
        margin: 5px;
        display: flex;
        align-items: center;
        justify-content: space-between;
    }
</style>