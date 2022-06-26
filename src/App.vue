<template>
  <div class="app">
    <MyHeader title="购物车案例" color="green"></MyHeader>
    <MyGoods></MyGoods>
    <MyFooter></MyFooter>
  </div>
</template>

<script>
import MyHeader from '#/MyHeader'
import MyGoods from '#/MyGoods'
import MyFooter from '#/MyFooter'
export default {
  data() {
    return {}
  },
  components: {
    MyHeader,
    MyGoods,
    MyFooter
  }
}
</script>

<style>
  .app {
    padding: 50px 0;
  }
</style>
