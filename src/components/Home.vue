<template lang="html">
  <el-breadcrumb separator="/" class="my-bread-menu">
    <el-breadcrumb-item :to="{ path: '/' }">首页</el-breadcrumb-item>
    <el-breadcrumb-item>活动管理</el-breadcrumb-item>
    <el-breadcrumb-item>活动列表</el-breadcrumb-item>
    <el-breadcrumb-item>活动详情</el-breadcrumb-item>
  </el-breadcrumb>
</template>

<script>
import myHeader from './Header.vue'
import leftMenu from './LeftMenu.vue'
export default {
}
</script>

<style lang="css" scoped>
  .my-bread-menu{margin-top: 20px;}
</style>
