<template>
  <div id="app">
    <img src="./assets/logo.png">
    <hello :msg='hei'></hello>
  </div>
</template>

<script>
import Hello from './components/Vue-text-dot.vue'

export default {
  name: 'app',
  components: {
    Hello
  },
  data () {
    return {
      hei: `的撒娇恐龙快打撒娇的快乐的撒艰苦拉萨的快乐就是大家快乐的撒看来的撒娇恐龙快打撒娇的快乐的撒艰苦拉萨的快乐就是大家快乐的撒看来
      的撒娇恐龙快打撒娇的快乐的撒艰苦拉萨的快乐就是大家快乐的撒看来
      的撒娇恐龙快打撒娇的快乐的撒艰苦拉萨的快乐就是大家快乐的撒看来
      的撒娇恐龙快打撒娇的快乐的撒艰苦拉萨的快乐就是大家快乐的撒看来
      的撒娇恐龙快打撒娇的快乐的撒艰苦拉萨的快乐就是大家快乐的撒看来的撒娇恐龙快打撒娇的快乐的撒艰苦拉萨的快乐就是大家快乐的撒看来的撒娇恐龙快打撒娇的快乐的撒艰苦拉萨的快乐就是大家快乐的撒看来
      的撒娇恐龙快打撒娇的快乐的撒艰苦拉萨的快乐就是大家快乐的撒看来的撒娇恐龙快打撒娇的快乐的撒艰苦拉萨的快乐就是大家快乐的撒看来的撒娇恐龙快打撒娇的快乐的撒艰苦拉萨的快乐就是大家快乐的撒看来的撒娇恐龙快打撒娇的快乐的撒艰苦拉萨的快乐就是大家快乐的撒看来
      的撒大撒旦`
    }
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
