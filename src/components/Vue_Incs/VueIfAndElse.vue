<script setup lang="ts">
const flag:boolean = true
const flag1:string = "A"
const message:string="<section>此处展示v-if/show用法, false隐藏 true显示</section>"
</script>

<template>
<!-- v-if约等于v-show false隐藏 true显示 -->
  <div v-show=flag v-html="message">
  </div>
  <!-- if-else语句 -->
  <div>
    <div v-if="flag1 == 'A'">A</div>
    <div v-else-if="flag1 == 'B'">B</div>
    <div v-else-if="flag1 == 'C'">C</div>
    <div v-else>D</div>
  </div>
</template>

<style lang="less">
</style>