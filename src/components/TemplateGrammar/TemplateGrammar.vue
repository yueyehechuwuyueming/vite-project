<script setup lang="ts">
// 在script声明变量可直接在template中使用
const message:string = '233333'
const message1:number = 0
const message2:string = "我,是,一,个,要,被,切,割,的,数,组,类,型"
</script>


<!-- 模板插值语法 -->
<template>
<!-- 一个div表示一个区域，division -->

<!-- 可替代下面{{message}}的写法 -->
  <div v-text="message">
  </div>

  <div>
    {{message}} 
    <!-- 支持编写条件运算 -->
    {{message1+1 ? '我是真的':'我是假的'}} 
    <!-- 支持操作API -->
    {{message2.split(',').map(v=> `￥${v}`)}}
  </div>

</template>

<style>

</style>
