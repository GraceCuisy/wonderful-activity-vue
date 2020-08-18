<template>
  <div class="indexContainer">
    <div class="header">
      <img src="../../assets/images/top.png" alt="">
    </div>
    <div class="contentWrap" ref="contentWrap">
      <button><a href="http:"></a></button>
      <div class="list">
        <div class="item" @click="handleClick">
          <img src="../../assets/images/first.png" alt=""/>
        </div>
        <div class="item" @click="handleClick">
          <img src="../../assets/images/first.png" alt="">
        </div>
        <div class="item" @click="handleClick">
          <img src="../../assets/images/first.png" alt="">
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import BScroll from '@better-scroll/core'
export default {
  name: 'index',
  mounted() {
    this.$nextTick(()=>{
      this.scroll=new BScroll(this.$refs.contentWrap,{
        scrollY:true,
      })
    })
  },
  methods: {
    handleClick(){
      window.location.href="https://hitokoto.cn/#"
    }
  },
}
</script>

<style lang="stylus" rel="stylesheet/stylus" scoped>
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
          width 654px
          height 252px
          border-radius 20px
          background-size cover
          box-shadow 6px 8px 25px 0px rgba(179, 41, 0, 0.75)
          margin-bottom 38px
          a
            display block
            width 100%
            height 100%
</style>
