<template>
  <div>
    <h1>Bicycle Rental Shop</h1>
    <p>Number of bicycles: {{ quantity }}</p>
    <p>Total income: {{ subtotalComputed }}</p>
  </div>
</template>

<script>
export default {
  name: 'BicycleRentalShop',
  data() {
    return {
      price: 100,
      quantity: 20
    }
  },
  computed: {
    subtotalComputed: function() {
      return this.price * this.quantity;
    }
  }
}
</script>

<style scoped>

</style>
