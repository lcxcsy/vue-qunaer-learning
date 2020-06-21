<template>
  <div class="header">
    <div class="header-left">
      <div class="iconfont back-icon">&#xe624;</div>
    </div>
    <div class="header-input">
      <span class="iconfont">&#xe632;</span>
      输入城市游玩主题
    </div>
    <router-link to="/city">
      <div class="header-right">
        {{ this.doubleCity }}
        <span class="iconfont arrow-icon">&#xe631;</span>
      </div>
    </router-link>
  </div>
</template>

<script>
import { mapState, mapGetters } from 'vuex'
export default {
  name: 'HomeHeader',
  computed: {
    ...mapState(['city']),
    ...mapGetters(['doubleCity'])
  }
}
</script>

<style lang="stylus" scoped>
@import '~sty/varibles.styl'

.header
  display: flex
  line-height: $headerHeight
  background: $bgColor
  color: #fff

.header-left
  width: $headerHeight
  float: left

  .back-icon
    text-align: center
    font-size: 0.4rem
    margin-top: 0.1rem

.header-input
  flex: 1
  height: $headerHeight
  line-height: $headerHeight
  padding-left: 0.2rem
  margin-top: 0.1rem
  margin-left: 0.2rem
  background: #fff
  border-radius: 0.1rem
  color: #ccc

.header-right
  min-width: 1.04rem
  padding: 0.1rem
  float: right
  text-align: center
  color: #fff

.arrow-icon
  font-size: 0.3rem
  margin-left: -0.04rem
</style>
