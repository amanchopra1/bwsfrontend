<template>
  <div class="language-selector">
    <label for="language" class="label">Select Language:</label>
    <select id="language" v-model="selectedLanguage" class="dropdown">
      <option v-for="language in languages" :key="language" :value="language">
        {{ language }}
      </option>
    </select>
  </div>
</template>

<script lang="ts">
import { defineComponent, ref } from 'vue';

export default defineComponent({
  name: 'LanguageSelector',
  setup() {
    const selectedLanguage = ref('');
    const languages = ref(['English', 'Hindi', 'Spanish', 'French']);
    return { selectedLanguage, languages };
  },
});
</script>

<style scoped>
.language-selector {
  text-align: center;
  margin-bottom: 20px;
}
.label {
  display: block;
  font-size: 18px;
  color: #32383b;
  margin-bottom: 5px;
}
.dropdown {
  padding: 10px;
  border: 1px solid #136cc7;
  border-radius: 5px;
  font-size: 16px;
}
</style>