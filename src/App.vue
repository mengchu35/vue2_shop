<template>
  <div id="app">
    <BicycleRentalShop></BicycleRentalShop>
    <TotalIncome></TotalIncome>
  </div>
</template>

<script>
import BicycleRentalShop from './components/BicycleRentalShop.vue'
import TotalIncome from './components/TotalIncome.vue'

export default {
  name: 'App',
  components: {
    BicycleRentalShop,
    TotalIncome
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
