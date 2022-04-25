<template>
  <div
    :class="[task.reminder ? 'reminder' : '', 'task']"
    @dblclick="$emit('toggle-reminder')"
  >
    <h3>
      {{ task.text }}
      <i @click="$emit('delete-task')" class="fas fa-times"></i>
    </h3>
    <p>{{ task.day }}</p>
  </div>
</template>


<script>
export default {
  name: "Task",
  props: {
    task: Object,
  },
};
</script>

<style scoped>
.task {
  background: #f4f4f4;
  margin: 5px;
  padding: 10px 20px;
  cursor: pointer;
}

.reminder {
  border-left: 5px solid green;
}

.task h3 {
  display: flex;
  align-items: center;
  justify-content: space-between;
}

.fas {
  color: red;
}
</style>