<script setup>
import Name from './components/Name.vue'
import Timeline from './components/Timeline.vue'
import Download from './components/Download.vue'
</script>

<template>
  <body>
    <Name/>
    <br>
    <Timeline/>
    <br>
    <Download/>
    <br>
  </body>
</template>

<style>
#app {
  font-family: Inter var,ui-sans-serif,system-ui,-apple-system,BlinkMacSystemFont,Segoe UI,Roboto,Helvetica Neue,Arial,Noto Sans,sans-serif,Apple Color Emoji,Segoe UI Emoji,Segoe UI Symbol,Noto Color Emoji;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  min-height: 100vh;
  padding-top: 20px;
}
</style>
