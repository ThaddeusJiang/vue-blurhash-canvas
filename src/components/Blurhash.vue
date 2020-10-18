<template>
  <canvas ref="canvas"></canvas>
</template>

<script>
import { decode } from "blurhash";

export default {
  props: {
    hash: String,
    width: {
      type: Number,
      default: 128,
    },
    height: {
      type: Number,
      default: 128,
    },
    punch: Number,
  },
  data() {},
  mounted() {
    const { hash, width, height, punch } = this.$props;
    const pixels = decode(hash, width, height, punch);
    const ctx = this.$refs.canvas.getContext("2d");
    const imageData = ctx.createImageData(width, height);
    imageData.data.set(pixels);
    ctx.putImageData(imageData, 0, 0);
  },
};
</script>
