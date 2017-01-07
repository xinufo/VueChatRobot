<template>
  <div class="leftContainer">
    <div class="top">
      <span></span>
      <p>小二狗</p>
    </div>
    <div class="bottom">
      <p>技术栈</p>
      <div class="container">
        <span class="msg col1">Vue 2.0</span>
        <span class="msg col2">Vue-resource</span>
        <span class="msg col3">webpack</span>
        <span class="msg col4">图灵机器人API</span>
        <div class="clear"></div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'left'
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.leftContainer {
  width: 265px;
  height: 480px;
  margin-right: 30px;
  float: left;
  box-shadow: 0 0 5px 0 #dbdada;
  background: #fff;
}

.top {
  height: 162px;
  padding-top: 40px;
  background: #00a3f0;
}

.top span {
  background: url(../assets/images/robot_head.jpg) no-repeat;
  height: 92px;
  width: 92px;
  display: block;
  margin: 0 auto;
  border-radius: 92px
}

.top p {
  text-align: center;
  color: #fff;
}

.bottom {
  padding-top: 10px;
}

.bottom p {
  padding: 12px 0 15px 30px;
}

.container {
  padding: 0 0 0 25px;
}

.msg {
  float: left;
  margin-right: 10px;
  margin-bottom: 16px;
  padding: 5px 12px;
  border-radius: 4px;
}

.col1 {
  color: #3cb1e7;
  border: #3cb1e7 solid 1px;
}

.col2 {
  color: #ff9c01;
  border: #ff9c01 solid 1px;
}

.col3 {
  color: #009944;
  border: #009944 solid 1px;
}

.col4 {
  color: #6e61a9;
  border: #6e61a9 solid 1px;
}
</style>
