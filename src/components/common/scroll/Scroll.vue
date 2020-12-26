<template>
  <div class="wrapper" ref="wrapper">
    <div class="content">
      <slot></slot>
    </div>
  </div>
</template>

<script>
import BScroll from 'better-scroll'

export default {
  name: 'Scroll',
  props: {
    probeType: {
      type: Number,
      default: 0
    },
    pullUpLoad: {
      type: Boolean,
      default: false
    }
  },
  data() {
    return {
      scroll: null
    }
  },
  mounted() {
    // 1. 创建bscroll对象
    this.scroll = new BScroll(this.$refs.wrapper,{
      observeDOM: true,
      click: true,
      // 这里不能将probeYype写死并不是每个使用这个scroll的实例都要使用这个probeType这一属性如果写死一些不需要的也会回调这个，会影响性能
      // probeType: 3
      probeType: this.probeType,
      pullUpLoad: this.pullUpLoad
    })
    // this.scroll.scrollTo(x,y)

    // 2. 监听滚动的位置
    this.scroll.on('scroll',(position) => {
      this.$emit('scroll', position)
    })

    // 3. 监听上拉事件
    this.scroll.on('pullingUp', () => {
      this.$emit('pullingUp')
    })
  },
  methods: {
    scrollTo(x, y, time=500) {
      this.scroll.scrollTo(x, y, time)
    },
    finishPullUp() {
      this.scroll.finishPullUp()
    }
  }
}

</script>
<style scoped>
</style>