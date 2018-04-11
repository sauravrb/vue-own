<template>
<div>
    <form>
      <input type="text" ref="my_input">
      <button @click.prevent="getFormValues()">Get values</button>
    </form>
    Output: {{ output }}
    </div>
</template>

<script>
export default {
  name: 'dateEntry',
  data () {
    return {
      output: ''
    }
  },
  methods: {
    getFormValues () {
      this.output = this.$refs.my_input.value
    }
  }
}
</script>
