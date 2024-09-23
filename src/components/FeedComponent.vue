<template>
  <div>
    <h3>Feed Money:</h3>
    <button v-on:click="addFunds(1)">$1</button>
    <button v-on:click="addFunds(5)">$5</button>
    <button v-on:click="addFunds(10)">$10</button>
    <button v-on:click="addFunds(0.05)">$0.05</button>
    <button v-on:click="addFunds(0.10)">$0.10</button>
    <button v-on:click="addFunds(0.25)">$0.25</button>
  </div>
</template>

<script>
export default {
  methods: {
    addFunds(amount) {
      this.$store.commit("INCREASE_FUNDS", amount);
    }
  }

}
</script>

<style>
  button {
    width: 113px;
    margin: 15px;
    border-radius: 20px;
  }
</style>