<template>
  <div>
    <div class="post-title">
      <h1>WAKKA</h1>
    </div>
    <div class="content" v-html="post.html" />
  </div>
</template>
<script>
export default {
  async asyncData({ params }) {
    try {
      let post = await import(`~/posts/${params.slug}.md`)
      console.debug(post)
      return {
        post
      }
    } catch (err) {
      console.debug(err)
      return false
    }
  }
}
</script>
