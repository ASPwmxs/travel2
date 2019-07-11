<template>
    <div class="wrapper">
        <swiper :options="swiperOption">
            <swiper-slide v-for="item of swiperList" :key="item.id">
                <img class="swiper-img" :src="item.imgUrl" />
            </swiper-slide>
            <div class="swiper-pagination"  slot="pagination"></div>
        </swiper>
    </div>
</template>

<script>
export default {
  name: 'HomeSwiper',
  data () {
    return {
      swiperOption: {
        pagination: '.swiper-pagination',
        loop: true // 让轮播插件支持循环轮播
      },
      swiperList: [{
        id: '0001',
        imgUrl: 'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20196/818f6cc784ae6669b74bbbb255414a53.jpg_750x200_66ca5873.jpg'
      }, {
        id: '0002',
        imgUrl: 'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20196/36358222d41ad18b66efe3dea09df24b.jpg_750x200_0005bed8.jpg'
      }]
    }
  }
}
</script>

<style lang="stylus" scoped>
    .wrapper >>> .swiper-pagination-bullet-active//样式穿透 不受scoped限制
        background:white!important
    .wrapper
        width:100%
        height:0
        overflow:hidden
        padding-bottom:27%
        background:#eee
        .swiper-img
            width:100%
</style>
