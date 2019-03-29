<template>
  <el-container class="navigation">
    <el-header class="header">
      <el-menu :default-active="activeIndex"
               class="el-menu-demo"
               mode="horizontal"
               @select="handleSelect"
               router="true">
        <el-menu-item index="路由1"><span class="img center"></span>处理中心</el-menu-item>
        <el-submenu index="路由2">
          <template slot="title">我的工作台</template>
          <el-menu-item index="2-1">选项1</el-menu-item>
          <el-menu-item index="2-2">选项2</el-menu-item>
          <el-menu-item index="2-3">选项3</el-menu-item>
          <el-submenu index="2-4">
            <template slot="title">选项4</template>
            <el-menu-item index="2-4-1">选项1</el-menu-item>
            <el-menu-item index="2-4-2">选项2</el-menu-item>
            <el-menu-item index="2-4-3">选项3</el-menu-item>
          </el-submenu>
        </el-submenu>
        <el-menu-item index="路由3"><span class="img center"></span>消息中心</el-menu-item>
        <el-menu-item index="路由4"><span class="img center"></span><a href="https://www.ele.me"
             target="_blank">订单管理</a></el-menu-item>
      </el-menu>
      <div class="line"></div>
    </el-header>
    <el-container>
      <el-aside class="aside">Aside</el-aside>
      <el-main>Main</el-main>
    </el-container>
  </el-container>
</template>
<script>
export default {
  data () {
    return {
      activeIndex: '1'
    }
  },
  methods: {
    handleSelect (key, keyPath) {
      console.log(key, keyPath);
    }
  },
}
</script>
<style lang="less" scoped>
.navigation {
  height: 100%;
  background-color: #fff;
  .header {
    // background-color: green;
    text-align: center;
    .el-menu-demo {
      display: inline-block;
    }
    .el-menu--horizontal > .el-menu-item.is-active {
      border-bottom: 2px solid #409eff;
      color: #303133;
      background-color: yellow;
    }
    .el-menu-item {
      padding: 0 40px;
    }
    .img {
      width: 20px;
      height: 20px;
      margin: 0 10px;
      background-color: skyblue;
      display: inline-block;
      // vertical-align: middle;
    }
  }
  .aside {
    width: 200px;
    background-color: gray;
  }
}
</style>
