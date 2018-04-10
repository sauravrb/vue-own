<template>
  <div id="app">
    <img src="./assets/logo.png">
    <router-view/>
    <form>
      <input type="text" ref="my_input">
      <button @click.prevent="getFormValues()">Get values</button>
    </form>

    Output: {{ output }}
  </div>
</template>

<script>
export default {
  name: 'App',
  data() {
    return {
      output: ''
    }
  },
  methods: {
    getFormValues() {
      debugger
      this.output = this.$refs.my_input.value
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
