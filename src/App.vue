<template>
  <div id="app">
    <index></index>
  </div>
</template>

<script>
import index from './components/index/index'
export default {
  name: 'App',
  components: {
    index
  }
}
</script>

<style lang="stylus" rel="stylesheet/stylus" scoped>
  #app
    width 100%
    height 100%
    overflow hidden
</style>
