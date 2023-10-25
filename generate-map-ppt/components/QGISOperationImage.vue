<script setup lang="ts">
import { ref } from 'vue'

const props = defineProps({
  count: {
    default: 0,
  },
  images: {
    default: [
      '/qgis/2.开启试验插件.png',
      '/qgis/3.安装HCMGIS插件.png',
      '/qgis/4.HCMGIS加载图层.png',
      '/qgis/5.OpenStreetMap图层.png',
    ]
  }
})

const counter = ref(props.count)




</script>

<template>
  <div>
    <div class="flex flex-row">
      <img
        v-for="(image, index) in props.images" 
        :key="index" 
        :src="image" 
        alt="" 
        class="w-1/2" 
      />
    </div>
    
    <div flex="~" w="min" border="~ gray-400 opacity-50 rounded-md">
      <button
        border="r gray-400 opacity-50"
        p="2"
        font="mono"
        outline="!none"
        hover:bg="gray-400 opacity-20"
        @click="counter -= 1"
      >
        -
      </button>
  
      <span m="auto" p="2">{{ counter }}</span>
      <button
        border="l gray-400 opacity-50"
        p="2"
        font="mono"
        outline="!none"
        hover:bg="gray-400 opacity-20"
        @click="counter += 1"
      >
        +
      </button>
    </div>
  </div>
</template>
