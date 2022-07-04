<template>
  <div id="app">
    <MainNav/>
    <router-view/>
  </div>
</template>


<script>
import MainNav from './components/MainNav'
 export default {
  name: 'App',
  components: {
    MainNav
  }
 }
</script>


<style lang="scss">
 html, body {
  margin: 0;
  padding: 0;
  text-align: center;
 }
</style>
