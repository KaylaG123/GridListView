<template>
  <div id="app">
    <product-list></product-list>

  </div>
</template>

<script>
import productList from './components/productList.vue'

export default {
  name: 'app',
  components: {
      productList,
  }
}
</script>

<style lang="scss">
#app {
    font-family: 'Avenir', Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
    margin-top: 60px;
}

</style>
