# VueChatRobot

> 基于Vue 2.0的简单聊天机器人 [在线演示](https://xinufo.github.io/demo/VueChatRobot/index.html)

- 样式不会写，直接搞了个和图灵机器人官网一样的

## 技术栈

- [vue 2.0](http://cn.vuejs.org/)
- [vue-resource](https://github.com/pagekit/vue-resource)
- [webpack](https://github.com/webpack/webpack)
- [图灵机器人API](http://www.tuling123.com/help/h_cent_webapi.jhtml?nav=doc)

## 总结

1. 父组件向子组件传数据使用属性，子组件向父组件传数据用事件
2. vue-resource发送json在main.js中设置Vue.http.options.emulateJSON = true
3. npm run build后资源路径错误需修改config/index.js中的build.assetsPublicPath

## 构建步骤

``` bash
# 安装依赖
npm install

# 启动测试服务器，地址localhost:8080，支持热更新
npm run dev

# 构建生产版本
npm run build
```

