<script setup lang="ts"></script>

<template>
  <div class="root">
    <div class="left"></div>
    <div class="container-box">
      <div class="header"></div>
      <div class="content">
        <div class="filter"></div>
        <div class="table-box">
          <div class="table">
            <div class="item" v-for="item in 50" :key="item" />
          </div>
        </div>
        <div class="page"></div>
      </div>
      <div class="footer"></div>
    </div>
  </div>
</template>

<style lang="scss">
.root {
  height: 100%;
  width: 100%;
  display: flex;
}
.left {
  width: 200px;
  height: 100%;
  background: #f4fad2;
}
.container-box {
  height: 100%;
  display: flex;
  flex: 1;
  overflow-y: auto;
  flex-direction: column;
  background: #d9d9d9;
  padding: 0 20px;
  .header {
    height: 60px;
    background: #fff;
  }
  .content {
    flex: 1;
    margin: 20px 0;
    background: #fff;
    display: flex;
    flex-direction: column;
    .filter {
      height: 60px;
      background: #acacac;
    }
    .table-box {
      flex: 1;
      // flex-basis: 0;
      margin-top: 12px;
      // 滚动
      // flex-basis: 0;
      // overflow: auto;
      .table {
        height: 100%;
        width: 100%;
        background: #a9c94f;
        .item {
          height: 30px;
          background: rebeccapurple;
          border-bottom: 1px solid #000;
          padding: 0 5px;
        }
      }
    }
    .page {
      margin-top: 12px;
      margin-bottom: 20px;
      height: 60px;
      background: #acacac;
    }
  }
  .footer {
    height: 60px;
    background: #fff;
  }
}

html,
body,
#app {
  width: 100%;
  height: 100%;
  padding: 0;
  margin: 0;
}
</style>
