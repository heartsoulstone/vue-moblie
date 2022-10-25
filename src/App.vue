<template>
  <div id="app">
    <van-tabs v-model="active" scrollspy>
      <van-tab v-for="index in 8" :title="'选项卡' + index" :key="index">
        内容{{index}}
      </van-tab>
    </van-tabs>
  </div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      active: 0
    }
  },
  methods: {}
};
</script>

<style>
.main-box {
  width: 100px;
  height: 100px;
  background: green;
}
.van-tabs {
  display: flex;
  justify-content: space-between;
}
/* 左侧导航栏 */
.van-tabs__nav {
  position: relative;
  display: block;
  background-color: #eeeeee;
  user-select: none;
}
.van-tabs__wrap--scrollable .van-tabs__nav {
  overflow-x: hidden;
  overflow-y: auto;
  -webkit-overflow-scrolling: touch;
}
.van-tabs__nav--line .van-tabs__nav--complete {
  padding-right: 0;
  padding-left: 0;
  position: fixed;
  left: 0;
}
.van-tabs__wrap {
  height: 100%;
  width: auto;
  overflow-y: auto;
}
.van-tabs__line {
  display: none;
}
.van-tab {
  position: relative;
  height: 50px;
  width: auto;
}
.van-tab--active {
  color: red;
}
.van-tab--active::before {
  position: absolute;
  top: 50%;
  left: 0;
  width: 4px;
  height: 16px;
  background-color: #ee0a24;
  transform: translate(-50%);
  content: ''
}
/* 右侧导航栏 */
.van-tabs__content {
  background-color: white;
  width: calc(100% - 94px);
  height: 100%;
  overflow-y: auto;
}
</style>
