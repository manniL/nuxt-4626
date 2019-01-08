<template>
  <div class="container">
    <div>
      <h1>
        Hello from <span class="name">{{ name }}</span
        >.
      </h1>
      <p><nuxt-link to="/" class="button--grey">Back home</nuxt-link></p>
    </div>
  </div>
</template>

<script>
export default {
  asyncData() {
    return {
      name: process.server ? 'server' : 'client'
    }
  }
}
</script>
