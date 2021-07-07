<template>
  <div class="row item-container" v-if="posts.length > 0">
    <div class="col-md-6 item marketing premium crm" v-for="(post, index) in posts" :key="index">
      <div id="googleCalendar" class="x-integration">
        <div class="widget-media">
          <img alt="image" :src="post.cover" class="x-int-img" />
        </div>
        <div class="widget-content">
          <div class="widget-section">
            <p class="x-int-title">{{ post.title }} <span class="x-type premium"></span></p>
            <p class="x-int-subtitle">{{ post.category }}</p>
            {{ post.description }}
          </div>
        </div>
      </div>
    </div>
  </div>
  <p v-else class="max-w-5xl mx-auto">Nothing Found</p>
</template>

<script>
export default {
  name: 'Integrations',
  data() {
    return {
      posts: [],
      postType: 'integration',
      loading: true,
    }
  },
  async mounted() {
    this.loading = true
    this.posts = await this.fetchPosts()
    this.loading = false
  },
  methods: {
    formatDate(dateString) {
      const date = new Date(dateString)
      return date.toLocaleDateString(process.env.lang) || ''
    },
    async fetchPosts(postType = this.postType) {
      return this.$content(postType)
        .fetch()
        .catch((err) => console.error(err) || [])
    },
  },
}
</script>
