<template>
  <div id="app">
    <BicycleRentalShop></BicycleRentalShop>
  </div>
</template>

<script>
import BicycleRentalShop from './components/BicycleRentalShop.vue'

export default {
  name: 'App',
  components: {
    BicycleRentalShop
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  /*text-align: center;*/
  color: #2c3e50;
  margin-top: 60px;
}
</style>
