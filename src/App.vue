<template>
  <div id="app">
    <img id="logo" src="./assets/vuetube-logo.png" alt="">
    <VideoPlayer />
  </div>
</template>

<script>
import VideoPlayer from './components/VideoPlayer'

export default {
  name: 'App',
  components: {
    VideoPlayer
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
}

#logo {
  width: 140px;
  margin: 14px;
}
</style>
