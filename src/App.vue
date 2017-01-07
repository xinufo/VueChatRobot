<template>
  <div id="app">
    <left></left>
    <right></right>
    <div class="clear"></div>
  </div>
</template>

<script>
import Left from './components/Left'
import Right from './components/Right'
import Msg from './components/Msg'

export default {
  name: 'app',
  components: {
    Left,
    Right,
    Msg
  }
}
</script>

<style>
body {
  background: #f9f9f9;
}

#app {
  width: 870px;
  margin: 50px auto 0px auto;
}

.clear {
  clear: both;
}
</style>
