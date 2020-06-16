<template>
  <div class="column is-one-third">
    <div class="post-item">
      <div class="frame">
        <img :src="post.indicatorImage" alt />
      </div>
      <h4 class="title is-5">{{ post.title }}</h4>
      <p class="summary">{{ post.body }}</p>
      <div class="info-container">
        <i class="far fa-calendar ml-1"></i>
        <span>{{ post.date }}</span>
        <i class="far fa-clock ml-1 mr-4"></i>
        <span>{{ post.time }}</span>
        <i class="far fa-comment-alt ml-1 mr-4"></i>
        <span>{{ post.commentsCount }}</span>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Post",
  props: {
    post: Object,
  },
};
</script>
