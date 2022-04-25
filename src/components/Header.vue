<template>
  <header>
    <h1>{{ title }}</h1>
    <Button
      :color="showAddTask ? 'red' : 'green'"
      @toggle-add-task="$emit('toggle-add-task')"
      :text="showAddTask ? 'Close' : 'Add Task'"
    />
  </header>
</template>

<script>
import Button from "./Button.vue";
export default {
  name: "Header",
  props: {
    title: {
      type: String,
    },
    showAddTask: Boolean,
  },
  components: {
    Button,
  },

  emits: ["toggle-add-task"],
};
</script>



<style scoped>
header {
  display: flex;
  justify-content: center;
  align-items: center;
  margin-bottom: 20px;
}
</style>