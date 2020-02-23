<template>
  <div id="app">
    <h4 class="bg-primary text-white text-center p-2">
      {{name}}'s To Do List
    </h4>
    <div class="row">
      <div class="col font-weight-bold">Task</div>
      <div class="col-2 font-weight-bold">Done</div>
    </div>
    <div class="row" v-for="t in tasks" v-bind:key="t.action">
      <div class="col">{{t.action}}</div>
      <div class="col-2">
        <input type="checkbox" v-model="t.done" class="form-check-input"/>
        {{t.done}}
      </div>
    </div>
  </div>
</template>

<script>

export default {
  name: 'App',
  data(){
    return{
      name: "Martin",
      tasks: [{ action: "Buy flowers", done: false},
      {action: "Practice German", done: true},
      {action: "Practice Vue", done: false},
      {action: "Work out", done: false}]
    }
  }
}
</script>

