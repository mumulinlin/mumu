<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <button @click="sendParent"></button>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: ['msg'],
  methods: {
    sendParent () {
      this.$emit('listenChild', 'mumu')
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="less">
h3 {
  margin: 40px 0 0;
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
