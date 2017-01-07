<template>
  <div class="message" v-bind:class="classType">
    <span class="header"></span>
    <p>
      {{MsgContent.msg.text}}
      <a v-bind:href="MsgContent.msg.url" v-if="MsgContent.msg.code === 200000">打开页面</a>
      <i></i>
    </p>
    <loader v-if="MsgContent.who === 'me' && MsgContent.status == 1" class="flag"></loader>
    <span v-if="MsgContent.who === 'me' && MsgContent.status == 2" class="flag err"></span>
    <div class="clear"></div>
  </div>
</template>

<script>
import Loader from './Loader'

// LOADING = 1
// ERROR = 2

export default {
  name: 'msg',
  components: {
    Loader
  },
  props: {
    MsgContent: ''
  },
  computed: {
    classType: function () {
      if (this.MsgContent.who === 'robot') {
        return 'robot'
      } else {
        return 'me'
      }
    }
  }
}
</script>

<style scoped>
.message {
  margin-bottom: 18px;
}

.robot .header {
  background: url(../assets/images/icons.png) no-repeat;
  height: 43px;
  width: 43px;
  background-position: 0 -666px;
  float: left;
  margin-left: 24px;
}

.me .header {
  background: url(../assets/images/icons.png) no-repeat;
  height: 40px;
  width: 40px;
  background-position: 0 -626px;
  float: right;
  margin-right: 28px;
}

p {
  margin: 0px;
  font-size: 14px;
  padding: 6px 18px;
  line-height: 24px;
  border-radius: 6px;
  position: relative;
  max-width: 220px;
  word-break: break-all;
}

.robot p {
  top: 4px;
  float: left;
  margin-left: 14px;
  color: #333;
  background: #f1f1f1;
  
}

.me p {
  top: 2px;
  float: right;
  margin-right: 14px;
  color: #fff;
  background: #19b955;
}

i {
  position: absolute;
  width: 0;
  height: 0;
  border-top: 6px solid transparent;
  border-bottom: 6px solid transparent;
  top: 12px;
}

.robot i {
  border-right: 6px solid #f1f1f1;
  left: -6px;
}

.me i {
  border-left: 6px solid #19b955;
  right: -6px;
}

.flag {
  position: relative;
  top: 11px;
  right: 7px;
  float: right;
}

.err {
  width: 15px;
  height: 15px;
  background: url(../assets/images/warning.png) no-repeat;
  color: red;
}
</style>