<template>
  <div class="header-container">
    <div class="l-container">
      <el-button
        icon="el-icon-menu"
        size="mini"
        @click="handleMenu"
      ></el-button>
      <span class="text">首页</span>
    </div>
    <div class="r-container">
      <el-dropdown>
        <span class="el-dropdown-link">
          <img class="userlogo" src="../assets/pander.webp" alt="" />
        </span>
        <el-dropdown-menu slot="dropdown">
          <el-dropdown-item>个人中心</el-dropdown-item>
          <el-dropdown-item>退出</el-dropdown-item>
        </el-dropdown-menu>
      </el-dropdown>
    </div>
  </div>
</template>

<script>
export default {
  name: 'CommonHeader',
  methods: {
    handleMenu() {
      this.$store.commit('CollapseMenu')
    }
  }
}
</script>

<style lang="less">
.header-container {
  padding: 0 20px;
  background-color: #333;
  height: 60px;
  display: flex;
  justify-content: space-between;
  align-items: center;
  .text {
    color: #fff;
    font-size: 10px;
    margin-left: 10px;
  }
  .r-container {
    .userlogo {
      width: 40px;
      height: 40px;
      border-radius: 50%;
    }
  }
}
</style>
