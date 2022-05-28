
<script>
import Platform from './components/Platform.vue'

export default {
  name: 'App',
  components: {
    Platform
  }
}
</script>
<template>
  <Platform/>
</template>
<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  height:100%;
}
html,body{
  height:100%;
  width:100%;
}
*{
  transition:all .15s linear;
}
</style>
