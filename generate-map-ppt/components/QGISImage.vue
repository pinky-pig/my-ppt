<script setup lang="ts">
const images = [
  '/qgis/2.开启试验插件.png',
  '/qgis/3.安装HCMGIS插件.png',
  '/qgis/4.HCMGIS加载图层.png',
  '/qgis/5.OpenStreetMap图层.png',
  '/qgis/6.下载高程数据.png',
  '/qgis/7.加载高程数据.png',
  '/qgis/8.修改高程颜色.png',
  '/qgis/9.下载行政区划数据.png',
  '/qgis/10.加载行政区划JSON.png',
  '/qgis/11.准备裁剪高程数据.png',
  '/qgis/12.裁剪高程数据.png',
  '/qgis/13.裁剪好高程数据.png',
  '/qgis/14.准备导出数据.png',
  '/qgis/15.导出高程.png',
  '/qgis/16.合并高程.png',
  '/qgis/17.合并高程数据完成.png',
  '/qgis/18.新建三维视图.png',
  '/qgis/19.三维效果配置.png',
  '/qgis/20.渲染三维效果.png',
  '/qgis/21.修改三维效果颜色.png',
]

</script>

<template>
  <img 
    v-for="(item, index) in images" 
    :key="item" 
    :src="item" 
    v-click 
    class="block w-fit absolute"
    style="height: -webkit-fill-available;" 
  />
</template>

