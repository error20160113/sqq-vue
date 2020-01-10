<template>
  <div class="app">
    <!-- <timer></timer>   -->
    <pic></pic>
  </div>
</template>

<script>
// import Timer from './components/Timer.vue'
import Pic from './components/Pic.vue'
export default {
  name: 'app',
  components: {
    // 'timer':Timer,
    'pic':Pic,
  }
}
</script>

<style scoped>

.app {
    width: 100%;
    height: 100%;
    /* background: pink; */
    text-align: center;

}
</style>
