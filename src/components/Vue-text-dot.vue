<template>
  <div>
    <p>{{pMsg}}</p>
  </div>
</template>

<script>
export default {
  name: 'vue-text-dot',
  props: {
    line: { type: Number, default: 3 },
    msg: { type: String, required: true }
  },
  data () {
    return {
      pMsg: this.msg,
      isDot: false
    }
  },
  mounted () {
    this.dot()
  },
  methods: {
    dot () {
      let dom = this.$el.querySelector('p')
      let height = parseInt(window.getComputedStyle(dom)['height'])
      let lineHeight
      if (window.getComputedStyle(dom)['line-height'] === 'normal') {
        console.error("[warn from vue-text-dot] you'd better set css 'line-height' ")
        lineHeight = parseInt(window.getComputedStyle(dom)['font-size']) * 1.5
      } else {
        lineHeight = parseInt(window.getComputedStyle(dom)['line-height'])
      }
      while (height > lineHeight * this.line * 3) {
        this.isDot = true
        this.pMsg = this.pMsg.substring(0, this.pMsg.length / 2)
        dom.innerHTML = this.pMsg
        height = parseInt(window.getComputedStyle(dom)['height'])
      }
      while (height > lineHeight * this.line) {
        this.isDot = true
        this.pMsg = this.pMsg.replace(/(\s)*([a-zA-Z0-9]+|\W)(\.\.\.)?$/,"...")
        dom.innerHTML = this.pMsg
        height = parseInt(window.getComputedStyle(dom)['height'])
      }
      if (this.isDot) {
        this.$emit('isDot')
      }
    },
  }
}
</script>
