<template>
  <div class="app">
    <pic></pic>
  </div>
</template>

<script>
import Pic from './components/Pic.vue'
export default {
  name: 'app',
  components: {
    'pic':Pic,
  }
}
</script>

<style scoped>

.app {
    width: 100%;
    height: 100%;
    background: pink;
    text-align: center;

}
</style>
