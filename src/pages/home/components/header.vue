<template>
    <div class="header">
        <div class="header-left">
            <div class="iconfont backicon">&#xe624;</div>
        </div>
        <div class="header-input">
             <span class="iconfont">&#xe632;</span>输入城市/景点/游玩主题</div>
        <router-link to="/city">
          <div class="header-right">{{this.city}} <span class="iconfont arrow-icon">&#xe6aa;</span></div>
        </router-link>
    </div>
</template>
<script>
//  1rem = html font-size = 50px
//     86/100
import { mapState } from 'vuex'
export default {
  name: 'HomeHeader',
  computed: {
    ...mapState(['city'])
  }
}
</script>
<style lang="stylus" scoped>
    @import '~styles/varibles.styl';
    .header
      display flex
      line-height .86rem
      background $bgColor
      color #ffffff
      .header-left
        width: .64rem
        float: left
        .backicon
            text-align center
            font-size .4rem
      .header-input
        flex: 1
        background #ffffff
        border-radius: .1rem
        line-height .64rem
        height: .64rem
        margin-top: .12rem
        margin-left: .2rem
        padding-left .2rem
        color: #ccc
      .header-right
        min-width  1.04rem
        padding 0.1rem
        float right
        text-align center
        color #ffffff
        .arrow-icon
            margin-left -.04rem
            font-size .24rem
</style>
