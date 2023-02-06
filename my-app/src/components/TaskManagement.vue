<template>
  <div>
    <div class="task-table">
      <table>
        <thead>
          <th>Title</th>
          <th>Content</th>
        </thead>
        <tbody>
          <tr v-for="(item, index) in tasks" :key="index">
            <td>{{ item.title }}</td>
            <td>{{ item.content }}</td>
          </tr>
        </tbody>
      </table>
    </div>
    <div class="task-form">
      <label>Title</label>
      <br />
      <input type="text" v-model="titleInput" />
      <br />
      <label>Content</label>
      <br />
      <textarea type="text" v-model="contentInput"></textarea>
    </div>
    <button class="add-btn" @click="addTask()" :disabled="!hasValidInput">
      Add task
    </button>
  </div>
</template>

<script lang="ts">
import Vue from "vue";
import { Task } from "@/interfaces/Task";

export default class TaskManagement extends Vue {
  tasks: Task[] = [];

  titleInput = "";
  contentInput = "";

  get hasValidInput() {
    return this.titleInput && this.contentInput;
  }

  addTask() {
    this.tasks.push({
      title: this.titleInput,
      content: this.contentInput,
    });
    console.log(this.tasks);
    this.titleInput = "";
    this.contentInput = "";
  }
}
</script>

<style scoped>
.task-table {
  background-color: aliceblue;
  display: 50%;
  margin-left: auto;
  margin-right: auto;
}

.add-btn {
  margin-top: 20px;
  padding: 20px;
  color: #42b983;
}
</style>
