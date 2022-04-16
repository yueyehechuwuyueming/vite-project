<script setup lang="ts">
const clickTap = () => {
    console.log("触发点击事件")
} 
</script>

<template>
 <!-- v-on:=@ 先触发子集，再触发父集，冒泡;-->
<div>
    <button v-on:click="clickTap">This is a button</button>
</div>
</template>

<style lang="less">
</style>