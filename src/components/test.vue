<template>
  <div id="app">
  <h1> {{msg}}</h1>
  <span v-bind:title="message">
    鼠标悬停几秒钟查看此处动态绑定的提示信息！
  </span>
  <button @click="changeOn()">点击展示</button>
  <button @click="changeOff()">点击隐藏</button>
  <p v-if="seen"> 查看到了信息</p>
  <ul>
    <li>{{ todo.text }}</li>
  </ul>
  </div>
</template>

<script>
export default {
  name: 'test',
  data () {
    return {
      msg: '跳转测试',
      message: '页面加载于 ' + new Date().toLocaleString(),
      seen: false
    }
  },
  methods: {
    changeOn () {
      this.$data.seen = true
    },
    changeOff () {
      this.$data.seen = false
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
