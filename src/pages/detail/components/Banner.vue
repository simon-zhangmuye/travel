<template>
  <div>
    <div class="banner" @click="handleBannerClick">
      <img class="banner-img"
           src="//img1.qunarzz.com/sight/p0/1602/59/59b3f674fa71203790.water.jpg_600x330_2b961b18.jpg"
      />
      <div class="banner-info">
        <div class="banner-title">中信国安第一城(AAAA景区)</div>
        <div class="banner-number"><span class="iconfont banner-icon">&#xe692;</span>11</div>
      </div>
    </div>
    <common-gallary :imgs="imgs"
                    v-show="showGallary"
                    @close="handleGallaryClose"
    ></common-gallary>
  </div>
</template>

<script>
import CommonGallary from 'common/gallary/Gallary'

export default {
  name: 'DetailBanner',
  components: {
    CommonGallary
  },
  data () {
    return {
      showGallary: false,
      imgs: ['http://img1.qunarzz.com/sight/p0/1602/59/59b3f674fa71203790.water.jpg_r_800x800_e2c7bf78.jpg',
        'http://img1.qunarzz.com/sight/p0/1602/b7/b7d5ce6723ec3c6e90.water.jpg_r_800x800_e6ef9e7c.jpg']
    }
  },
  methods: {
    handleBannerClick () {
      this.showGallary = true
    },
    handleGallaryClose () {
      this.showGallary = false
    }
  }
}
</script>

<style lang="stylus" scoped>
  .banner
    position: relative
    height: 0
    padding-bottom: 55%
    overflow: hidden
    .banner-img
      width: 100%
    .banner-info
      display: flex
      position: absolute
      left: 0
      right: 0
      bottom: 0
      line-height: .6rem
      color: #fff
      background-image: linear-gradient(top, rgba(0, 0, 0, 0), rgba(0, 0, 0, 0.8))
      .banner-title
        flex: 1
        font-size: .32rem
        padding: 0 .2rem
      .banner-number
        height: .32rem
        line-height: .32rem
        margin-top: .14rem
        padding: 0 .4rem
        border-radius: .2rem
        background: rgba(0, 0, 0, .8)
        .banner-icon
          font-size: .24rem
          margin-right: .06rem
</style>
