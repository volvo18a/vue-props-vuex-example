<template>
  <div class="god">
    <h1>{{ msg1 }}</h1>
  </div>
</template>

<script>
export default {
  name: 'god',
  data () {
    return {
      msg1: '',
      fff: 'abc'
    }
  },
  props: ['msg'],
  mounted () {
    this.msg1 = this.msg
    console.log(this.fff)
    console.log(this.$store.state.count)
    this.$emit('getChild', this.fff)
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
