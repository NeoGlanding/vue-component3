<template>
  <p>Hello</p>
  <PassThroughComp />
</template>

<script>
import PassThroughComp from './components/PassThroughComp.vue'

export default {
  name: 'App',
  components: {
    PassThroughComp
  },
  data() {
    return {
      friends: ['Eko', 'Kurniawan', 'Khannedy']
    }
  },
  provide() {
    return {
      friends: this.friends 
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
