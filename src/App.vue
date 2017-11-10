<template>
  <div id="app" unselectable="on" onselectstart="return false;">
    <router-view/>
  </div>
</template>

<script>
export default {
  name: 'app'
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #fff;
  margin-top: 120px;
  -moz-user-select: none;
  -webkit-user-select: none;
}

body {
  height: 100vh;
  width: 100vw;
  overflow: hidden;
}
</style>
