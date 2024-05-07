<template>
  <div>
    <!-- 组件：可以复用 -->
    <button @click="increment">+</button>
    <button v-on:click="decrement">-</button>
    <p>子组件num {{num}} </p>
    <p>props {{$props.num}} </p>
    <!-- html赋值 -->
    <p><span>html赋值</span><span v-html="num"></span></p>
    <p><span>text赋值</span><span v-text="num"></span></p>
    <!-- 表示 -->
    <p>表达式：{{num % 2?'奇数':'偶数'}}</p>
  </div>
</template>

<script>
export default{
  props:['num','incre'],   // 子组件接收值
  data() {
    return {
      //num:0
    }
  },
  methods:{
    increment(){  // 加
      this.incre()
    },
    decrement(){
      // 自定义事件使用，不需要接收
      this.$emit('decre')
    }
  }
}
</script>

<style>
</style>
