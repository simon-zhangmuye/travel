<template>
    <div>
      <div class="recommend-title">热销推荐</div>
      <ul v-for="item of recommendList" :key="item.id">
        <li class="item border-bottom">
            <img class="item-img" :src="item.imgUrl" />
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
      recommendList: [
        {
          id: '0001',
          imgUrl: 'http://img1.qunarzz.com/sight/p0/1510/e1/e1c111149b76d49b90.img.jpg_200x200_66e41130.jpg',
          title: '霸州茗汤温泉',
          desc: '阿尔卡迪亚御临泉温泉'
        }, {
          id: '0002',
          imgUrl: 'http://img1.qunarzz.com/sight/p0/1510/e1/e1c111149b76d49b90.img.jpg_200x200_66e41130.jpg',
          title: '霸州茗汤温泉',
          desc: '阿尔卡迪亚御临泉温泉'
        }, {
          id: '0003',
          imgUrl: 'http://img1.qunarzz.com/sight/p0/1510/e1/e1c111149b76d49b90.img.jpg_200x200_66e41130.jpg',
          title: '霸州茗汤温泉',
          desc: '阿尔卡迪亚御临泉温泉'
        }
      ]
    }
  },
  components: {}
}
</script>
<style lang="stylus" scoped>
  @import '~styles/mixins.styl'
  .recommend-title
    margin-top: .2rem
    line-height: .8rem
    background: #eee
    text-indent: .2rem
  .item
    overflow: hidden
    display: flex
    height: 1.9rem
    .item-img
      width: 1.7rem
      height: 1.7rem
      padding: .1rem
    .item-info
      flex: 1
      padding: .1rem
      min-width: 0
      .item-info
        line-height: .54rem
        font-size: .32rem
        ellipsis()
      .item-desc
        line-height: .4rem
        font-size: .28rem
        color: #ccc
        ellipsis()
      .item-button
        background: #ff9300
        padding: 0 .01rem
        border-radius: .06rem
        margin-top: .16rem
        color: #fff
        line-height: .44rem
</style>
