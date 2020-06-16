<template>
  <div class="column is-one-third">
    <div class="post-item">
      <div class="frame">
        <img :src="post.indicatorImage" alt />
      </div>
      <h4 class="title is-5">{{post.title}}</h4>
      <p class="summary">{{post.body}}</p>
      <div class="info-container">
        <i data-feather="calendar"></i>
        <span>{{post.date}}</span>
        <i data-feather="clock" class="mr-4"></i>
        <span>{{post.time}}</span>
        <i data-feather="message-square" class="mr-4"></i>
        <span>{{post.commentsCount}}</span>
      </div>
    </div>
  </div>
</template> 

<script>
export default {
  name: "Post",
  props: {
    post: Object
  }
};
</script>
