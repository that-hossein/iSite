<template>
  <section class="section">
    <div class="container">
      <transition-group name="list" tag="div" class="columns is-multiline">
        <Post v-for="post in posts" :key="post.id" :post="post" />
      </transition-group>
    </div>
  </section>
</template>

<script>
import Post from "./Post.vue";
export default {
  components: {
    Post
  },
  props: {
    posts: Array
  }
};
</script>

<style scoped>
.list-enter-active,
.list-leave-active {
  transition: all 1s;
}

.list-enter,
.list-leave-to {
  /* .list-leave-active below version 2.1.8 */
  opacity: 0;
  transform: scale(0.9);
}
</style>