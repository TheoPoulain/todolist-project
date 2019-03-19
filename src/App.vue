<template>
    <div id="app" class="container">
        <img src="./assets/logo.png" class="logo">
        
        <Todos></Todos>
        <CurrentTodos></CurrentTodos>
        <CompletedTodos></CompletedTodos>

        <!-- <router-view/> -->
    </div>
</template>

<script>
    import Todos from './components/Todos.vue'
    import CurrentTodos from './components/CurrentTodos.vue'
    import CompletedTodos from './components/CompletedTodos.vue'

    import 'bootstrap/dist/css/bootstrap.css'
    import 'bootstrap-vue/dist/bootstrap-vue.css'

    export default {
        name: 'App',
        components: {
          Todos,
          CurrentTodos,
          CompletedTodos
        }
    }
</script>

<style>

* {
  box-sizing: border-box;
}

.container {
  max-width: 600px;
  margin: 0 auto;
}

.logo {
  display: block;
  margin: 0 auto;
  height: 100px;
}

#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  font-size: 20px;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  /* text-align: center; */
  color: #2c3e50;
  margin-top: 60px;
}
</style>