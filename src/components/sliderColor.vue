<script setup lang="ts">
import { ref, computed } from 'vue'

defineProps<{ msg: string }>()

const sliderValue = ref(0)

const randomColor = computed(() => {
  const hue = 60
  const saturation = Math.floor(Math.random() * 100)
  const lightness = Math.floor(Math.random() * 100)
  return `hsl(${hue}, ${saturation}%, ${lightness}%)`
})
</script>

<template>
  <div :style="{ background: randomColor }">
    <p>マウスでスライドしてみよう</p>
    <form>
      <input type="range" className="slider" v-model="sliderValue" min="0" max="255">
    </form>
    {{ sliderValue }}
  </div>
</template>

<style scoped>
.read-the-docs {
  color: #888;
}
</style>