<template>
  <div>
    <h1>{{ post.title }}</h1>
    <div>{{ post.body }}</div>
  </div>
</template>

<script>
import posts from '~~/posts'

export default {
  props: {

  },

  components: {

  },

  computed: {
    post() {
      let id = this.$route.params.id
      return this.posts.find(post => {
        return post.id == id
      })
    }
  },

  methods: {
    
  },

  data() {
    return {
      posts
    }
  },
}

</script>