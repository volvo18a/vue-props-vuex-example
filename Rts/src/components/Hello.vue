<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <God :msg="msg" v-on:getChild="getData"></God>
    <Go :msg="msg" v-on:getChild="getData"></Go>
  </div>

</template>

<script>
import God from '@/components/God'
import Go from '@/components/Go'

export default {
  name: 'hello',
  components: {
    God,
    Go
  },
  data () {
    return {
      msg: 'Welcome to Your Vue.js App',
      ggg: ''
    }
  },
  methods: {
    getData (fff) {
      console.log(fff)
      this.ggg = fff
      console.log(this.ggg)
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
