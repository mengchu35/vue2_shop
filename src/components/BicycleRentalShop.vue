<template>
  <div>
    <h1>Bicycle Rental Shop</h1>
    <p>Number of bicycles: {{ count }}</p>
    <button v-on:click="plus" v-bind:disabled="btnPlus()">+1</button>
    <button v-on:click="minus" v-bind:disabled="btnMinus()">-1</button>
    <p v-if="count == 0">No bike is available</p>
    <p v-else>Bikes are available</p>
    <!--<p>Total income: {{ subtotalComputed }}</p>-->
  </div>
</template>

<script>
export default {
  name: 'BicycleRentalShop',
  data() {
    return {
      price: 100,
      quantity: 20, // 總量
      count: 20, // 剩餘個數
    }
  },
  computed: {
    subtotalComputed: function() {
      return this.price * this.quantity;
    }
  },
  methods: {
    plus() {
      this.count++;
    },
    minus() {
      this.count--;
    },
    btnPlus() {
      return ((this.count >= this.quantity) ? true : false);
    },
    btnMinus() {
      return ((this.count <= 0) ? true : false);
    },
  }
}
</script>

<style scoped>

</style>
