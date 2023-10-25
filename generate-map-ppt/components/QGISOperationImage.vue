<script setup lang="ts">
import { ref } from 'vue'

const props = defineProps({
  count: {
    default: 0,
  },
})

const counter = ref(props.count)


// const svgFiles = await getAllImage()

// // 从单个文件目录获取原始文件内容
// async function getAllImage() {
//   const images = await Promise.all(
//     Object.entries(
//       import.meta.glob('/src/qgis/*.png', { as: 'raw' }))
//       .map(async ([path, resolver]) => {
//         debugger
//         return {
//           raw: await resolver(),
//           title: (path as any).split('/').pop().split('.')[0],
//           path,
//         }
//       }),
//   )
//   return images
// }

</script>

<template>
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
</template>
