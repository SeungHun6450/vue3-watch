<template>
  <h1 @click="changeMessage">
    {{ msg }}
  </h1>
  <h1>{{ reversedMessage }}</h1>
</template>

<script>
export default {
  data() {
    return {
      msg: 'Hello?'
    }
  },
  computed: {
    reversedMessage() {
      return this.msg.split('').reverse().join('')
    }
  },
  watch: {
    // 해당하는 부분을 감시하고 있어서 바뀐 내용이 감지가 되면 바뀐것을 볼 수 있다.
    msg(value) {
      // console.log('msg : ', this.msg)
      console.log('msg : ', value)
    },
    reversedMessage(value) {
      // console.log('reversedMessage : ', this.reversedMessage)
      console.log('reversedMessage : ', value)
    }
  },
  methods: {
    changeMessage() {
      this.msg = 'Good!'
    }
  }
}
</script>