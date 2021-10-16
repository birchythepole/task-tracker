<template>
  <button @click="$emit('btn-click')" :style="{backgroundColor: color}" class="btn">{{ text }}</button>
</template>

<script>
export default {
  name: "Button",
  props: {
    text: {
      type: String,
      default: "Default Button",
    },
    color: {
      type: String,
      default: "rgb(1,1,1)",
    },
  },
  emits:['btn-click']
};
</script>