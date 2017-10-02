<template>
  <div id="app">
    <!--<img src="./assets/logo.png">-->
   <!-- <hello></hello> -->
   <todo-list v-bind:todos="todos"></todo-list>
  </div>
</template>

<script>
import TodoList from './components/TodoList';

export default {
  name: 'app',
  components: {
    TodoList,
  },
  data() {
    return {
      todos: [{
        title: 'TODO A',
        project: 'Project A',
        done: 'false',
      }, {
        title: 'TODO B',
        project: 'Project B',
        done: 'true',
      }, {
        title: 'TODO C',
        project: 'Project C',
        done: false,
      }, {
        title: 'TODO D',
        project: 'Project D',
        done: false,
      }],
    };
  },
};
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
