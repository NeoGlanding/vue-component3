<template>
  <p>Hello</p>
  <PassThroughComp :selected="selected" />
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
      friends: ['Eko', 'Kurniawan', 'Khannedy'],
      selected: ''
    }
  },
  provide() {
    return {
      friends: this.friends,
      selected: this.selected,
      selectFriends: this.selectFriends, 
    }
  },
  methods: {
    selectFriends(name) {
      this.selected = name;
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
