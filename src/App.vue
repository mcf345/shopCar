<template>
  <div class="app">
    <MyHeader title="购物车案例" color="green"></MyHeader>
    <MyGoods v-for="item in goodsList" :key="item.goods_id" :goods="item"></MyGoods>
    <MyFooter :goodsList="goodsList"></MyFooter>
  </div>
</template>

<script>
import MyHeader from '#/MyHeader'
import MyGoods from '#/MyGoods'
import MyFooter from '#/MyFooter'
import axios from 'axios'
export default {
  data() {
    return {
      goodsList: []
    }
  },
  components: {
    MyHeader,
    MyGoods,
    MyFooter
  },
  created() {
    this.getGoods()
  },
  methods: {
    async getGoods() {
      const res = await axios({ url: '/api/cart' })
      this.goodsList = res.data.list
    }
  }
}
</script>

<style>
.app {
  box-sizing: border-box;
  max-height: 100vh;
  padding: 50px 0;
  overflow: auto;
}
</style>
