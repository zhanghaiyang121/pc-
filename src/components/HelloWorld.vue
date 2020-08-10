<template>
  <div class="body">
    <div class="left">
      <el-menu
        default-active="2"
        class="el-menu-vertical-demo"
        background-color="#545c64"
        text-color="#fff"
        active-text-color="#ffd04b"
        @open="handleOpen"
        @close="handleClose">
        <el-submenu index="1">
          <template slot="title">
            <i class="el-icon-location"></i>
            <span>导航一</span>
          </template>
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
          <i class="el-icon-menu"></i>
          <span slot="title">导航二</span>
        </el-menu-item>
        <el-menu-item index="3" disabled>
          <i class="el-icon-document"></i>
          <span slot="title">导航三</span>
        </el-menu-item>
        <el-menu-item index="4">
          <i class="el-icon-setting"></i>
          <span slot="title">导航四</span>
        </el-menu-item>
      </el-menu>
    </div>
    <div class="right">
      <div class="head"></div>
      <div class="content_box">
        <div class="itembox" v-for="item in 20"></div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  methods:{
    handleOpen(key, keyPath) {
      console.log(key, keyPath);
    },
    handleClose(key, keyPath) {
      console.log(key, keyPath);
    }
  }
}
</script>

<style>
.html{
  font-size: 19.2px;
}
.body{
  width:100%;
  height: 100%;
  display: flex;
}
.left{
  width:300px;
  height: 100%;
  background: #545c64;
}
.right{
  width:1620px;
  height: 100%;
  background: blue;
  display: flex;
  flex-direction: column;
}
.head{
  height: 50px;
  background: pink;
  width: 100%;
}
.content_box{
  width:100%;
  flex: 1;
  overflow: auto;
  display: flex;
  flex-wrap:wrap;
  justify-content: space-around;
}
.el-button{
  width:300px
}
.itembox{
  background: yellow;
  width: 750px;
  height: 400px;
  border-radius: 20px;
  margin: 10px;
}
</style>