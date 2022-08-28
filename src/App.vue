<template>
  <!-- <img alt="Vue logo" src="./assets/logo.png"> -->
  <h1>WURFL Device Detector Tool</h1>
  <detection/>
</template>

<script>
import detection from './components/detection.vue'

export default {
  name: 'App',
  components: {
    detection
  },
}

</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  /* text-align: center;
  color: #2c3e50; */
  margin-top: 60px;
}
</style>
