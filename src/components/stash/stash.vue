<script setup lang="ts">
// 在script声明变量可直接在template中使用
const message:string = '233333'
const message1:number = 0
const message2:string = "我，是，一，个，人"
const message3:string="<section>2222222</section>"

const flag:boolean = false
const flag1:string = "A"

const parent = () => {
  console.log('我是父集');
}
const clickTap = () => {
  console.log('我是子集');
}


type Style = {
  color:string,
  height:string
}

const style1:Style = {
  color:"pink",
  height:"2000px"
}
</script>


<!-- 模板插值语法 -->
<template>
<!-- 一个div表示一个区域，division -->

<!-- 可替代下面{{message}}的写法 -->
  <div v-text="message">
  </div>

<!-- v-html可以渲染标签，展示富文本 -->
<!-- v-if约等于v-show false隐藏 true显示 -->
  <div v-show=flag v-html="message3">
  </div>
  <div>
    {{message}} 
    <!-- 支持编写条件运算 -->
    {{message1+1 ? '我是真的':'我是假的'}} 
    <!-- 支持操作API -->
    {{message2.split('，').map(v=> `￥${v}`)}}
  </div>

  <!-- if-else语句 -->
  <div>
    <div v-if="flag1 == 'A'">A</div>
    <div v-else-if="flag1 == 'B'">B</div>
    <div v-else-if="flag1 == 'C'">C</div>
    <div v-else>D</div>
  </div>

  <!-- v-on:=@ 先触发子集，再触发父集，冒泡;-->
  <!-- 加stop，不影响父集，阻止冒泡 -->
  <div @click="parent">
    <button @click.stop="clickTap">123</button>
  </div>
<!-- 阻止表单提交(阻止界面刷新) 加prevent-->
  <form action="/">
    <button @click.prevent="clickTap">提交</button>
    <!-- <button type="submit">提交</button> -->
  </form>

  <div v-bind:style="style1">
    我是233333
  </div>
  233
  <div :class="['a','b']">我是class类生成的2333</div>

</template>

<style>
.a{
  color:red
}

.b{
  height:300px
}
</style>
