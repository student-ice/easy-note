<script setup>
function newBtnClicked() {
  console.log('new')
}
function exitBtnClicked() {
  window.api.sendExitSignal()
}
</script>

<template>
  <div class="titlebar">
    <button class="new" @click="newBtnClicked">新建</button>
    <span>easy-note</span>
    <button class="exit" @click="exitBtnClicked">退出</button>
  </div>
</template>

<style>
.titlebar {
  display: flex;
  justify-content: space-between;
  height: 50px;
  position: fixed;
  left: 0;
  top: 0;
  right: 0;
  background-color: antiquewhite;
  -webkit-app-region: drag;
}
.titlebar span {
  line-height: 50px;
}
.titlebar button {
  width: 30px;
  height: 30px;
  background-color: white;
  border: none;
  align-self: center;
  -webkit-app-region: no-drag;
}
.titlebar .new {
  margin-left: 5px;
}
.titlebar .exit {
  margin-right: 5px;
}
.titlebar .new:hover {
  background-color: antiquewhite;
}
</style>
