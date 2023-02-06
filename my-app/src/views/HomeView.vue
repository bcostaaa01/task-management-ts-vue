<template>
  <div class="home">
    <TaskManagement />
  </div>
</template>

<script lang="ts">
import { Component, Vue } from "vue-property-decorator";
import TaskManagement from "@/components/TaskManagement.vue";

@Component({
  components: {
    TaskManagement,
  },
})
export default class HomeView extends Vue {}
</script>
