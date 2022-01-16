<template>
  <header>
    <h1>{{ title }}</h1>
    <Button
      @btn-clicked="$emit('btn-clicked')"
      :text="btnShown ? 'Close' : 'Add task'"
      :color="btnShown ? 'red' : 'green'"
    />
  </header>
</template>

<script>
import Button from "./Button";
export default {
  name: "Header",
  props: {
    title: String,
    btnShown: Boolean,
  },
  data() {
    return {
      text: "Add task",
    };
  },
  components: {
    Button,
  },
  emits: ["btn-clicked"],
};
</script>

<style scoped>
header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 20px;
}
</style>
