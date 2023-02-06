<template>
  <div>
    <div class="task-table">
      <table>
        <thead>
          <th>Title</th>
          <th>Content</th>
        </thead>
        <tbody>
          <tr>
            <td></td>
            <td></td>
          </tr>
        </tbody>
      </table>
    </div>
    <div class="task-form">
      <label>Title</label>
      <br />
      <input type="text" />
      <br />
      <label>Content</label>
      <br />
      <input type="text" />
    </div>
    <button>Add task</button>
  </div>
</template>

<script lang="ts">
import Vue from "vue";
import Task from "@/interfaces/Task";

export default class TaskManagement extends Vue {
    tasks: Task[] = [];
}
</script>
