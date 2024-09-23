<template>
  <div id="main-area">
    <ProductsComponent id ="prod-area"/>
    <FeedComponent id ="feed-money-area"/>
    <FundsComponent id ="funds-area"/>
  </div>
</template>

<script>
import ProductsComponent from './components/ProductsComponent.vue';
import FeedComponent from './components/FeedComponent.vue';
import FundsComponent from './components/FundsComponent.vue';

export default {
  components: {ProductsComponent, FeedComponent, FundsComponent}
}
</script>

<style>
  #main-area {
    display: grid;
    grid-template-columns: 1fr 1fr;
    grid-template-areas: 
      "feed funds"
      "prod prod";
  }

  #feed-money-area {
    grid-area: feed;
  }

  #funds-area {
    grid-area: funds;
  }

  #prod-area {
    grid-area: prod;
  }

</style>