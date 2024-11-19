<template>
  <div class="app">
    <LanguageSelector />
    <div class="card-container">
      <Card title="Yoga and Pranayama" color="#136cc7" />
      <Card title="Mindfulness Meditation" color="rgb(232, 179, 208)" />
      <Card title="Relaxation Music" color="rgb(216, 91, 158)" />
      <Card title="Mantras and Kirtan" color="#32383b" />
    </div>
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue';
import LanguageSelector from './components/LanguageSelector.vue';
import Card from './components/Card.vue';

export default defineComponent({
  name: 'App',
  components: {
    LanguageSelector,
    Card,
  },
});
</script>

<style scoped>
.app {
  text-align: center;
  background-color: #fdfeff;
  min-height: 100vh;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}
.card-container {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  margin-top: 20px;
}
</style>