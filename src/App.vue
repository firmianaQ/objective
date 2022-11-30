<template>
  <div id="app">
    <div class="container"></div>
  </div>
</template>

<script setup lang="ts">
import Cropper from "cropperjs";
import { onMounted } from "vue";

const init = () => {
  const image = new Image();
  image.src = "https://fengyuanchen.github.io/cropperjs/v2/picture.jpg";
  new Cropper(image, {
    container: ".container",
    template: `<cropper-canvas style="height:400px" background>
          <cropper-image></cropper-image>
          <cropper-handle action="select" plain></cropper-handle>
          <!--选区1-->
          <cropper-selection class="selection" x="10" y="5" width="160" height="90" initial-coverage="0" movable resizable zoomable multiple>
            <cropper-grid role="grid" bordered covered></cropper-grid>
            <cropper-crosshair theme-color="rgba(238, 238, 238, 0.5)" centered></cropper-crosshair>
            <cropper-handle class="inner" action="move" theme-color="rgba(255, 255, 255, 0.15)"></cropper-handle>
            <cropper-handle action="n-resize"></cropper-handle>
            <cropper-handle action="e-resize"></cropper-handle>
            <cropper-handle action="s-resize"></cropper-handle>
            <cropper-handle action="w-resize"></cropper-handle>
            <cropper-handle action="ne-resize"></cropper-handle>
            <cropper-handle action="nw-resize"></cropper-handle>
            <cropper-handle action="se-resize"></cropper-handle>
            <cropper-handle action="sw-resize"></cropper-handle>
          </cropper-selection>
           <!--选区2-->
          <cropper-selection class="selection" x="180" y="5" width="200" height="50" initial-coverage="0"  resizable zoomable multiple>
            <cropper-grid role="grid" bordered covered></cropper-grid>
            <cropper-crosshair theme-color="rgba(238, 238, 238, 0.5)" centered></cropper-crosshair>
            <cropper-handle class="inner" action="move" theme-color="rgba(255, 255, 255, 0.15)"></cropper-handle>
            <cropper-handle action="n-resize"></cropper-handle>
            <cropper-handle action="e-resize"></cropper-handle>
            <cropper-handle action="s-resize"></cropper-handle>
            <cropper-handle action="w-resize"></cropper-handle>
            <cropper-handle action="ne-resize"></cropper-handle>
            <cropper-handle action="nw-resize"></cropper-handle>
            <cropper-handle action="se-resize"></cropper-handle>
            <cropper-handle action="sw-resize"></cropper-handle>
          </cropper-selection>
        </cropper-canvas>`,
  });
};

onMounted(() => init());
</script>

<style scoped>
.container {
  width: 500px;
}
</style>
