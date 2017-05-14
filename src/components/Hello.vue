<template>
  <el-row class="container">
    <el-col :span="24" class="header">
      <el-col :span="3">
        <h3>
          帐融
          <span style="color:#EF4836;">通</span>
        </h3>
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
    <el-col :span="24" class="main">
      <aside class="sideBar">
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
      </aside>
      <section class="content">
        <el-breadcrumb separator="/">
          <el-breadcrumb-item :to="{ path: '/' }">首页</el-breadcrumb-item>
          <el-breadcrumb-item>活动管理</el-breadcrumb-item>
          <el-breadcrumb-item>活动列表</el-breadcrumb-item>
          <el-breadcrumb-item>活动详情</el-breadcrumb-item>
        </el-breadcrumb>
        <div class="line"></div>
        <div class="content-wrapper">
          <h2>供应商</h2>
          <div class="m-heading-1 border-green m-bordered">
            <h3>项目编号：P201704130003&nbsp;&nbsp;
              <el-tag type="danger">已受理</el-tag>
            </h3>
            <p>应收帐款债权所有人：供应商测试帐号</p>
            <p>供应商：供应商测试帐号</p>
          </div>
          <el-steps :space="100" :active="2" finish-status="success">
            <el-step title="转让申请(供应商)"></el-step>
            <el-step title="转让受理(保理商)"></el-step>
            <el-step title="应收帐款确权(核心企业)"></el-step>
            <el-step title="复核(保理商)"></el-step>
            <el-step title="拟定合同(保理商)"></el-step>
            <el-step title="签订合同(供应商)"></el-step>
            <el-step title="通知确认(核心企业)"></el-step>
            <el-step title="付款(保理商)"></el-step>
            <el-step title="收款确认(供应商)"></el-step>
          </el-steps>
          <div class="portlet bordered">
             应收帐款转让申请 
          </div>
        </div>
      </section>
    </el-col>
  </el-row>
</template>

<style scoped lang="scss">
.container {
  height: 100%;
  .header {
    background-color: #2b3643;
    font-weight: 300;
    color: #fff;
    height: 60px;
    line-height: 60px;
    text-align: center;
    .tools {
      float: left;
      margin-left: 20px;
    }
  }
  .main {
    display: flex;
    height: calc(100% - 60px);
    .sideBar {
      flex: 0 0 230px;
      width: 230px;
      height: 100%;
      weight: 300;
      text-align: left;
      font-weight: 300;
      .el-menu {
        height: 100%;
        overflow-y: auto;
      }
    }
    .content {
      flex: 1;
      overflow-y: auto;
      padding: 20px;
      .line {
        height: 1px;
        background: #e7ecf1;
        margin: 10px -20px 0 -20px;
      }
      .content-wrapper {
        h2 {
          font-weight: normal;
          font-weight: 300;
          color: #666;
          margin: 25px 0;
        }
        h3 {
          margin-bottom: 15px;
        }
        p {
          margin-top: 10px;
          font-size: 14px;
        }
        .portlet{
          margin-top:25px;
          padding:12px 20px 15px 20px;
          border-radius: 4px;
        }
      }
    }
  }
}
</style>
