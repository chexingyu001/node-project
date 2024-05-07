<template>
  <div>
    <!-- 使用组件-组件标签 -->
    <h1>hello world</h1>
    <!-- 将值传给子组件,将方法传递给子组件,v-on:自定义事件,省略写法@decre="decrement" -->
    <count :num="num" :incre="icrement" @decre="decrement"></count>
    <!-- <count v-bing:num="num"></count> -->
    <p>这是父组件的值{{num}}</p>
  </div>
</template>

<script>
  import count from './count.vue' // 导入组件（子组件）
  export default {
    name: 'HelloWorld',
    data() {
      return {
        num:10,   // 定义一个数据
        msg: 'Welcome to Your Vue.js App'
      }
    },
    methods:{
      // 定义方法，修改自己的值
      icrement(){
        this.num++
      },
      decrement(){
        this.num--
      }
    },
    // 注册(映射)组件
    components: {
      count //
    }
  }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
