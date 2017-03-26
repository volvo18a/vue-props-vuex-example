<template>
  <div class="go">
    <h1>{{ msg1 }}</h1>
  </div>
</template>

<script>

export default {
  name: 'go',
  data () {
    return {
      msg1: '',
      aaa: 2
    }
  },
  props: ['msg'],
  mounted () {
    this.msg1 = this.msg
    console.log(this.$store.state.count)
  },
  updated () {
    this.$store.state.count = this.aaa
    console.log(this.$store.state.count)
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
