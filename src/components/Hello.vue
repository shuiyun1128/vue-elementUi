<template>
  <el-row class="container">
    <el-col :span="24" class="header">
      <el-menu theme="dark" :default-active="activeIndex" class="el-menu-demo" mode="horizontal" @select="handleSelect">
        <el-menu-item index="1">处理中心</el-menu-item>
        <el-submenu index="2">
          <template slot="title">我的工作台</template>
          <el-menu-item index="2-1">选项1</el-menu-item>
          <el-menu-item index="2-2">选项2</el-menu-item>
          <el-menu-item index="2-3">选项3</el-menu-item>
        </el-submenu>
        <el-menu-item index="3">
          <a href="https://www.ele.me" target="_blank">订单管理</a>
        </el-menu-item>
      </el-menu>
    </el-col>
    <el-col :span="4" class="sideBar">
      <el-menu default-active="2" class="el-menu-vertical-demo" @open="handleOpen" @close="handleClose" theme="dark">
        <el-submenu index="1">
          <template slot="title">
            <i class="el-icon-message"></i>管理员控制台</template>
          <el-menu-item-group>
            <template slot="title">分组一</template>
            <el-menu-item index="1-1">选项1</el-menu-item>
            <el-menu-item index="1-2">选项2</el-menu-item>
          </el-menu-item-group>
          <el-menu-item-group title="分组2">
            <el-menu-item index="1-3">选项3</el-menu-item>
          </el-menu-item-group>
          <el-submenu index="1-4">
            <template slot="title">选项4</template>
            <el-menu-item index="1-4-1">选项1</el-menu-item>
          </el-submenu>
        </el-submenu>
        <el-menu-item index="2">
          <i class="el-icon-menu"></i>导航二</el-menu-item>
        <el-menu-item index="3">
          <i class="el-icon-setting"></i>导航三</el-menu-item>
      </el-menu>
    </el-col>
    <el-col :span="20" class="main">
      <div>管理员控制台</div>
    </el-col>
  </el-row>
</template>

<style scoped lang="scss">
.container {
  .header {
    .el-menu {
      background-color: #2b3643;
      font-weight: 300;
    }
  }
  .sideBar {
    position: fixed;
    top: 60px;
    left: 0;
    min-height: calc(100% - 60px);
    background-color: #324157;
    font-weight: 300;
  }
}
</style>
