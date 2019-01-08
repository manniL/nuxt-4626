<template>
  <div class="container"><nuxt /></div>
</template>
<script>
export default {
  computed: {
    theme() {
      return /about/.test(this.$route.path) ? 'red' : 'blue'
    }
  },
  head() {
    return {
      htmlAttrs: {
        class: this.theme,
        theme: this.theme
      }
    }
  }
}
</script>

<style>
.red {
  background-color: palevioletred;
}
.blue {
  background-color: lightblue;
}
</style>
