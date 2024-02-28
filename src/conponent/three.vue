<script setup></script>
<template>
  <div class="header">
    <div class="contrast">
      <div class="menu active borderRight">补充协议1</div>
      <div class="menu borderRight">补充协议2</div>
      <div class="menu">补充协议3</div>
    </div>
    <a-button type="primary">新增</a-button>
  </div>
  <div class="contain">
    <div class="contain_flex">
      <div class="contrastContent">协议内容：</div>
      <a-button class="delect">删除</a-button>
    </div>
    <a-textarea v-model:value="value" class="text" :rows="4" />
  </div>
  <div class="save">
    <a-button type="primary">保存</a-button>
  </div>
</template>
<style scoped>
.delect {
  color: rgb(253, 148, 1);
}
.header {
  margin-top: 10px;
  display: flex;
  justify-content: space-between;
  padding: 0 10px;
  align-items: center;
}
.contrast {
  display: flex;
  border: 1px solid #ccc;
  border-bottom: none;
}
.menu {
  padding: 10px 20px;
  color: rgb(138, 138, 138);
  background: #fff;
  font-size: 12px;
}
.active {
  color: rgb(23, 145, 254);
  font-weight: bold;
  font-size: 14px;
}
.borderRight {
  border-right: 1px solid #ccc;
}
.contain {
  margin: 0 10px;
  background: #fff;
  padding: 0 13px;
  border: 1px solid #ccc;
}
.contrastContent {
  margin-top: 10px;
  font-size: 12px;
}
.contain_flex {
  height: 40px;
  display: flex;
  justify-content: space-between;
  align-items: center;
}
.text {
  margin-bottom: 30px;
  background: rgb(248, 248, 248);
}
.save {
  padding: 10px;
  margin-top: 20px;
  background: #fff;
}
</style>
