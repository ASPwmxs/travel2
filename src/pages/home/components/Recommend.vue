<template>
    <div>
        <div class="title">热销推荐</div>
        <ul>
            <li class="item border-bottom" v-for="(item,index) of recommendList" :key="index">
                <div class="item-imgwrapper">
                    <img class="item-img" :src="item.imgUrl" />
                </div>
                <div class="item-info">
                    <p class="item-title">{{item.title}}</p>
                    <p class="item-desc">{{item.desc}}</p>
                    <button class="item-button">查看详情</button>
                </div>
            </li>
        </ul>
    </div>
</template>

<script>
export default {
  name: 'HomeRecommend',
  data () {
    return {
      recommendList: [{
        id: '0001',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1508/2e/d9363ce50a88c8c5ff5a138c67687cd4.water.jpg_200x200_1c15c8f5.jpg',
        title: '深圳野生动物园',
        desc: '国际啤酒节清凉一夏'
      }, {
        id: '0002',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1808/48/48ae3e0f9a3f195ca3.img.jpg_200x200_f2195465.jpg',
        title: 'Skyland未来科技馆',
        desc: '深圳新的亲子游乐打卡圣地'
      }, {
        id: '0003',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1902/80/80d7d3ef350b7fffa3.water.jpg_200x200_01e78b60.jpg',
        title: '东部华侨城茶溪谷',
        desc: '🔥好评如潮，小伙伴热推景点~'
      }]
    }
  }
}
</script>

<style lang="stylus" scoped>
    @import '~styles/mixins.styl'
    .title
        margin-top: .2rem
        line-height: .8rem
        background:#eee
        text-indent: .2rem
    .item
        overflow:hidden
        display:flex
        height:1.9rem
        .item-img
            width:1.7rem
            height:1.7rem
            padding:.1rem
        .item-info
            flex:1
            padding:.1rem
            min-width:0
            .item-title
                line-height: .54rem
                font-size:.32rem
                ellipsis()
            .item-desc
                line-height:.4rem
                color:#ccc
                ellipsis()
            .item-button
                line-height:.44rem
                margin-top:.16rem
                background:#ff9300
                padding:0 .1rem
                border-radius:.06rem
                color:#fff
</style>
