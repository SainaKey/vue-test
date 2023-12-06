<script setup lang="ts">
import { ref } from 'vue'

defineProps<{ msg: string }>()

const sliderValue = ref(0)

</script>

<template>
  <div>
    <p>こんにちは～</p>
      <form>
        <input type="range" className="slider" v-model="sliderValue" min="0" max="255">
      </form>
      {{sliderValue}}1
  </div>
</template>

<style scoped>
.read-the-docs {
  color: #888;
}
</style>
