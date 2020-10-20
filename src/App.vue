<template>
  <div id="app">
    <SalesReport> </SalesReport>
  </div>
</template>

<script>
import SalesReport from './components/SalesReport'
export default {
  name: 'App',
  components: {
    SalesReport
  }
}
</script>

<style>
html, body {
  width: 100%;
  height: 100%;
  margin: 0;
  padding: 0;
  background-color: #ccc;
}
#app {
  width: 100%;
  height: 100%;
  padding: 20px;
  box-sizing: border-box;
}
</style>
