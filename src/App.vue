<template>
  <div id="app">
    <div class="indexContainer">
      <div class="header">
        <img src="./assets/images/top.png" alt="">
      </div>
      <div class="contentWrap" ref="contentWrap">
        <div class="list">
          <div class="item">
            <a href="https://www.baidu.com">
              <img src="./assets/images/first.png" alt="">
            </a>
          </div>
          <div class="item">
            <a href="https://www.baidu.com">
              <img src="./assets/images/first.png" alt="">
            </a>
          </div>
          <div class="item">
            <a href="https://www.baidu.com">
              <img src="./assets/images/first.png" alt="">
            </a>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import BScroll from '@better-scroll/core'
export default {
  name: 'App',
  mounted() {
    this.$nextTick(()=>{
      this.scroll=new BScroll(this.$refs.contentWrap,{
        scrollY:true,
        click:true,
      })
    })
  },
}
</script>

<style lang="stylus" rel="stylesheet/stylus" scoped>
  #app
    width 100%
    height 100%
    overflow hidden
    .indexContainer
      width 100%
      height 100%
      background-color #FFBC9D
      .header
        width 100%
        height 478px
        img 
          width 100%
          height 478px
      .contentWrap
        width 100%
        height calc(100vh - 480px)
        padding-left 48px
        padding-right 48px
        overflow hidden
        .list
          padding-bottom 20px
          .item
            position relative
            display block
            width 654px
            height 252px
            border-radius 20px
            background-size cover
            box-shadow 6px 8px 25px 0px rgba(179, 41, 0, 0.75)
            margin-bottom 38px
            a
              position absolute
              left 0
              top 0
              width 100%
              height 100%
              z-index 5

</style>
