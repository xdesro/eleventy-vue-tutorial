<template>
  <nav>
    <a href="/">Home</a>
    <ul>
      <li v-for="post in posts">
        <a :href="`/posts/${post.slug}/`">{{ post.title }}</a>
      </li>
    </ul>
  </nav>
</template>

<script>
export default {
  props: ["posts"],
};
</script>
