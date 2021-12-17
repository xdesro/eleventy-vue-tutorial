<template>
  <div>
    <h1>{{ post.title }}</h1>
    <div v-html="body" />
  </div>
</template>

<script>
const markdownRenderer = require("markdown-it")();

export default {
  data() {
    return {
      pagination: {
        size: 1,
        data: "posts",
        alias: "post",
      },
      permalink: (data) => `posts/${data.post.slug}/index.html`,
      eleventyComputed: {
        title: (data) => data.post.title,
      },
    };
  },
  computed: {
    body() {
      return markdownRenderer.render(this.post.content);
    },
  },
};
</script>
