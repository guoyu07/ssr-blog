<!-- ./components/Posts.vue -->
<template>
  <div class="list">
    <ul v-for="post in posts">
      <li>
        <p>{{ post.title }}</p>
        <p>{{ post.summary }}</p>
        <p>{{ post.published }}</p>
        <nuxt-link :to="`/post/${post.id}`" class="card-footer-item">Read More</nuxt-link>
      </li>
    </ul>
  </div>
</template>

<script>
  import posts from '~/posts.json'

  export default {
    name: 'posts',
    data () {
      return { posts }
    }
  }
</script>

<style type="text/css">
  *{
    margin: 0;
    padding: 0;
  }
  .list li{
    list-style: none;
    padding:10px;
    margin: 20px auto;
    text-align: left;
  }
  .list p{
    line-height: 30px;
  }
</style>
