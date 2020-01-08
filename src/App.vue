<template>
  <div class="app">
    <div style="height:10%"></div>
    <timer></timer>
    <div style="width:100%; position:fixed; bottom:0;">
      <!-- <span>开始于2018-10-23 08:30:00</span> -->
    </div>
  </div>
</template>

<script>
import Timer from './components/Timer.vue'

export default {
  name: 'app',
  components: {
    'timer':Timer
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
