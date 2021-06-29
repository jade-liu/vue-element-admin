<template>
  <div id="app" class="page-component__scroll">
    <el-scrollbar class="scrollbar">
      <div id="nav" class="nav-class">
        <router-link to="/">Home</router-link> |
        <router-link to="/about">About</router-link>
      </div>
      <router-view />
    </el-scrollbar>
    <el-backtop
      target=".page-component__scroll .el-scrollbar__wrap"
      :bottom="100"
      :visibility-height="50"
    ></el-backtop>
  </div>
</template>

<style lang="scss" scoped>
.scrollbar {
  height: calc(100vh - 60px);
}
/deep/.el-scrollbar__wrap {
  overflow-x: hidden;
}
</style>
