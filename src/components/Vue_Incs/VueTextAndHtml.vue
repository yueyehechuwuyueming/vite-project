<script setup lang="ts">
const text1:string = '此处展示v-text语法'
const html1:string = "<section>此处展示v-html语法</section>"

</script>

<template>
  <div v-text="text1"></div>
  <!-- v-html可以渲染标签，展示富文本 -->
  <div v-html="html1"></div>
</template>

<style lang="less">
</style>