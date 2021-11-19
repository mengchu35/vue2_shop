<template>
  <div>
    <h1>Bicycle Rental Shop</h1>
    <p>Number of bicycles: {{ count }}</p>
    <button v-on:click="plus" v-bind:disabled="btnPlus">+1</button>
    <button v-on:click="minus" v-bind:disabled="btnMinus">-1</button>
    <p v-if="count == 0">No bike is available</p>
    <p v-else>Bikes are available</p>
    <p>Rules</p>
    <ol>
      <li v-for="(rule, index) in rules" v-bind:key="index">{{ rule }}</li>
    </ol>
    <TotalIncome v-bind:incrementTotal="increment" v-on:resetall="reset"></TotalIncome>
  </div>
</template>

<script>
import TotalIncome from './TotalIncome.vue'

export default {
  name: 'BicycleRentalShop',
  components: {
    TotalIncome
  },
  data() {
    return {
      price: 100,
      quantity: 20, // 總量
      count: 20, // 剩餘個數
      increment: 0, // 租借次數
      rules: [
        '$100 each time.',
        'Please return no later than 18:00.',
        'Be safe.'
      ],
    }
  },
  computed: {
    btnPlus() {
      return ((this.count >= this.quantity) ? true : false);
    },
    btnMinus() {
      return ((this.count <= 0) ? true : false);
    }
  },
  methods: {
    plus() {
      this.count++;
    },
    minus() {
      this.count--;
      this.increment++;
    },
    reset() {
      this.count = 20;
      this.increment = 0;
    }
  }
}
</script>

<style scoped>

</style>
