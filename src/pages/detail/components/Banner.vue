<template>
    <div>
        <div class="banner" @click="handleBannerClick">
            <img class="banner-img" src="//img1.qunarzz.com/sight/p0/1508/2e/d9363ce50a88c8c5ff5a138c67687cd4.water.jpg_600x330_28bda6b0.jpg" />
            <div class="banner-info">
                <div class="banner-title">深圳野生动物园(AAAA景区)</div>
                <div class="banner-number">
                    <span class="iconfont banner-icon">&#xe692;</span>
                    39
                </div>
            </div>
        </div>
        <common-gallary :imgs="imgs" v-show="showGallary" @close="handleGallaryClose"></common-gallary>
    </div>
</template>

<script>
import CommonGallary from 'common/gallary/Gallary'
export default {
  name: 'DetailBanner',
  data () {
    return {
      showGallary: false,
      imgs: ['http://img1.qunarzz.com/sight/p0/1507/61/fb7a04aed1b537261fc17f57bce9a12c.water.jpg_r_800x800_d8cfa479.jpg', 'http://img1.qunarzz.com/sight/p0/1508/f1/bdbf2ec42b17550c71620042e09e217c.water.jpg_r_800x800_3703d9e5.jpg']
    }
  },
  methods: {
    handleBannerClick () {
      this.showGallary = true
    },
    handleGallaryClose () {
      this.showGallary = false
    }
  },
  components: {
    CommonGallary
  }
}
</script>

<style lang="stylus" scoped>
  .banner
    position: relative
    overflow:hidden
    height:0
    padding-bottom:55%
    .banner-img
        width:100%
    .banner-info
        display:flex
        position:absolute
        left:0
        right:0
        bottom:0
        line-height: .6rem
        color:#fff
        background-image: linear-gradient(top, rgba(0,0,0,0),rgba(0,0,0,0.8))
        .banner-title
            flex:1
            font-size: .32rem
            padding: 0 .2rem
        .banner-number
            height: .32rem
            padding: 0 .4rem
            line-height: .32rem
            margin-top: .14rem
            border-radius: .2rem
            background: rgba(0,0,0, .8)
            font-size:.24rem
            .banner-icon
                font-size:.24rem
</style>
