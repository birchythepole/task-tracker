<template>
  <header>
    <h1>{{ title }}</h1>
    <Button @btn-click="$emit('btn-click')" text="Add Task" color='rgb(50, 145, 65)'/>
  </header>
</template>
<script>
import Button from './Button.vue'
export default {
  name: 'Header',
  components:{
      Button
  },
  props: {
    title: {
        type: String,
        default: 'Default Title'
    }
  },
  emits:['btn-click']

};
</script>

<style scoped>
header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 20px;
}
</style>