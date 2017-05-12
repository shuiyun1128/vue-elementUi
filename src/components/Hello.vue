<template>
  <el-row class="container clearfix">
    <el-col :span="24" class="header">
      <el-col :span="3">
        帐融<span style="color:#EF4836;">通</span>
      </el-col>
      <el-col :span="17">
        <div class="tools">
          <i class="fa fa-align-justify"></i>
        </div>
      </el-col>
      <el-col :span="4" class="userinfo">
        <el-dropdown trigger="hover">
          <span class="el-dropdown-link userinfo-inner"></span>
          <el-dropdown-menu slot="dropdown">
            <el-dropdown-item>我的消息</el-dropdown-item>
            <el-dropdown-item>设置</el-dropdown-item>
            <el-dropdown-item divided>退出登录</el-dropdown-item>
          </el-dropdown-menu>
        </el-dropdown>
      </el-col>
    </el-col>
    <el-col :span="3" class="sideBar">
      <el-menu default-active="2" class="el-menu-vertical-demo" theme="dark">
        <el-submenu index="1">
          <template slot="title">
            <i class="el-icon-message"></i>管理员控制台
          </template>
          <el-menu-item-group>
            <el-menu-item index="1-1">系统控制台</el-menu-item>
            <el-menu-item index="1-2">项目列表</el-menu-item>
            <el-menu-item index="1-3">供应商列表</el-menu-item>
            <el-menu-item index="1-4">保理商列表</el-menu-item>
            <el-menu-item index="1-5">核心企业列表</el-menu-item>
            <el-menu-item index="1-6">用户列表</el-menu-item>
          </el-menu-item-group>
        </el-submenu>
        <el-submenu index="2">
          <template slot="title">
            <i class="el-icon-message"></i>系统设置
          </template>
          <el-menu-item-group>
            <el-menu-item index="2-1">系统设置</el-menu-item>
            <el-menu-item index="2-2">系统日志</el-menu-item>
          </el-menu-item-group>
        </el-submenu>
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
    background-color: #2b3643;
    font-weight: 300;
    color: #fff;
    height: 60px;
    line-height: 60px;
    .tools {
      float: left;
      margin-left: 20px;
    }
  }
  .sideBar {
    position: fixed;
    top: 60px;
    left: 0;
    min-height: calc(100% - 60px);
    background-color: #364150;
    font-weight: 300;
    text-align: left;
    .el-menu-vertical-demo {
      background-color: #364150;
    }
  }
}
</style>
