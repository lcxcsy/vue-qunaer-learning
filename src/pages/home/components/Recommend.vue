<template>
  <div>
    <div class="title">
      <div class="iconfont love-icon">&#xe613;</div>
      <div class="title-title">猜你喜欢</div>
    </div>
    <ul>
      <router-link tag="li"
                   class="item border-bottom"
                   v-for="item of list"
                   :key="item.id"
                   :to="'/detail/' + item.id">
        <img class="item-img"
             :src="item.imgUrl" />
        <div class="item-info">
          <p class="item-title">{{ item.title }}</p>
          <p class="item-desc">{{ item.desc }}</p>
          <button class="item-button">查看详情</button>
        </div>
      </router-link>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HomeRecommend',
  props: {
    list: Array
  }
}
</script>

<style lang="stylus" scoped>
@import '~sty/mixins.styl'

.title
  margin-top: 0.2rem
  line-height: 0.8rem
  background: #eeeeee
  text-indent: 0.2rem
  .love-icon
    display: inline
    text-align: left
    font-size: 0.46rem
    color: red
  .title-title
    display: inline
    font-size: 0.34rem
    margin-left: 0.1rem
.item
  display: flex
  overflow: hidden
  height: 1.9rem
  .item-img
    width: 1.7rem
    height: 1.7rem
    padding: 0.1rem
  .item-info
    flex: 1
    padding: 0.1rem
    min-width: 0
    .item-title
      line-height: 0.54rem
      font-size: 0.32rem
      ellipsis()
    .item-desc
      line-height: 0.4rem
      color: #ccc
      ellipsis()
    .item-button
      line-height: 0.44rem
      margin-top: 0.16rem
      background: #ff9300
      padding: 0 0.1rem
      border-radius: 0.06rem
      color: white
</style>
