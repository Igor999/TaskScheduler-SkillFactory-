<template>
  <div id="app">
    <shop shop-title="Смартфоны" />
    <shop :shop-title="{title: 'Ноутбуки'}" />
  </div>
</template>

<script>
  import Shop from "./components/Shop";

  export default {
    components: {
      Shop
    }
  }
</script>

<style scoped lang="scss">
#app {
  font-family: 'Roboto', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

#nav {
  padding: 30px;

  a {
    font-weight: bold;
    color: #2c3e50;

    &.router-link-exact-active {
      color: #42b983;
    }
  }
}
</style>
