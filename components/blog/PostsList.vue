<template>
  <section class="post-list">
    <div class="container">
      <div class="posts__wrapper">
        <PostPreview v-for="post in posts" :key="post.id" :post="post" />
      </div>
    </div>
  </section>
</template>

<script>
import PostPreview from "@/components/blog/PostPreview.vue";
export default {
  components: {
    PostPreview,
  },
  props: {
    posts: {
      type: Array,
      required: true,
    },
  },
};
</script>

<style lang="scss">
.posts__wrapper {
  display: flex;
  align-items: flex-end;
  justify-content: space-between;
  flex-wrap: wrap;
}
</style>
