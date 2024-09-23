<template>
  <div class="container">
    <ItemComponent
      v-for="item in $store.state.products"
      v-bind:key="item.id"
      v-bind:item="item"
    ></ItemComponent>
  </div>
</template>

<script>
import ItemComponent from './ItemComponent.vue';

export default {
  components: {ItemComponent}
}
</script>

<style>
    .container {
        display: flex;
        justify-content: center;
        flex-wrap: wrap;
        padding: 20px;
    }

</style>