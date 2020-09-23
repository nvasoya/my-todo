<template>
  <div id="app">
      <Todos v-bind:todos="todoList"  />
  </div>
</template>

<script>
import Todos  from './components/Todos';

export default {
  name: 'App',
  components: {
    Todos
  },
  data() {
    return {
      todoList : [
        {
          id: 1,
          title: "Task 1",
          isComplete : false
        },{
          id: 2,
          title: "Task 2",
          isComplete : false
        },
        {
          id: 3,
          title: "Task 3",
          isComplete : true
        },{
          id: 4,
          title: "Task 4",
          isComplete : false
        }
      ]
    }
  }

}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
