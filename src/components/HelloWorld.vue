<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <h2 @click="getMsg">哈哈哈</h2>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data () {
    return {
      msg: '欢迎你~'
    }
  },
  methods: {
    getMsg(){
      console.log(this.msg)
    }
  },
}
</script>

<style scoped>
h1, h2 {
  font-weight: normal;
}
</style>
