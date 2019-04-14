<template>
  <div id="app">
    <el-scrollbar>
      <img
        alt="Vue logo"
        src="./assets/logo.png"
      >
      <HelloWorld msg="Welcome to Your Vue.js App" />
      <el-table :data="tableData">
        <el-table-column
          prop="date"
          label="日期"
          width="140"
        >
        </el-table-column>
        <el-table-column
          prop="name"
          label="姓名"
          width="120"
        >
        </el-table-column>
        <el-table-column
          prop="address"
          label="地址"
        >
        </el-table-column>
      </el-table>
    </el-scrollbar>
  </div>
</template>

<script>
import HelloWorld from "./components/HelloWorld.vue";

export default {
  name: "app",
  components: {
    HelloWorld
  },
  data() {
    const item = {
      date: "2016-05-02",
      name: "王小虎",
      address: "上海市普陀区金沙江路 1518 弄"
    };
    return {
      tableData: Array(20).fill(item)
    };
  }
};
</script>

<style>
html {
  background: red;
  height: 100%;
}

body {
  background: yellow;
  height: 100%;
  margin: 0;
}

#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  background: blue;
  height: 100%;
}

/* 需要设置 el-scrollbar 的高度，具体数值或100%，使用100%时父层高度要固定。 */
.el-scrollbar {
  height: 100%;
}

/* 隐藏横向滚动条 */
.el-scrollbar__wrap {
  overflow-x: hidden;
}
</style>
