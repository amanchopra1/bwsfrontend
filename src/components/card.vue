<template>
  <div class="card" :style="{ backgroundColor: color }">
    <h3 class="title">{{ title }}</h3>
  </div>
</template>

<script lang="ts">
import { defineComponent, PropType } from 'vue';

export default defineComponent({
  name: 'Card',
  props: {
    title: {
      type: String,
      required: true,
    },
    color: {
      type: String,
      required: true,
    },
  },
});
</script>

<style scoped>
.card {
  width: 250px;
  height: 150px;
  margin: 10px;
  display: flex;
  justify-content: center;
  align-items: center;
  border-radius: 10px;
  box-shadow: 0px 4px 8px rgba(0, 0, 0, 0.1);
  text-align: center;
  color: #fdfeff;
}
.title {
  font-size: 18px;
  font-weight: bold;
}
</style>