<template>
  <div class="container">
    <div v-if="error.statusCode === 404" class="page">
      <nuxt-link to="/">
          404
      </nuxt-link>
    </div>
    <div v-else class="page">
      <nuxt-link to="/">
        暂无页面
      </nuxt-link>
    </div>
  </div>
</template>

<script>
  export default {
    props: ['error'],
    layout: 'blog'
  }
</script>

<style scoped>
  .page img{width: 80%;padding-top: 60px; display: block; margin:0 auto}
</style>