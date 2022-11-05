<template>
  <div v-for="task of tasks">
    <Task :text="task" />
  </div>
  <input type="text" v-model="newTaskName">
  <button @click="addTask">
    Add
  </button>
</template>

<script>
import Task from './components/Task.vue';
export default {
  data() {
    return {
      tasks: ["do the laundry", "vaccuum the floor", "walk the dog", "register for clockhacks", "apsdhfpasdh"],
      username: "Jay",
      username2: "bob",
      numClicks: 0,
      newTaskName: "",
    }
  },
  methods: {
    addTask() {
      this.tasks.push(this.newTaskName);
      this.newTaskName = "";
    }
  },
  components: {
    Task
  }
}
</script>

<style>
#jay {
  color: green;
}

button {
  padding: 3px;
}

button:hover {
  padding: 5px;
}
</style>
