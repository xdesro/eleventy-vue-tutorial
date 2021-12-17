<template>
  <article>
    <Navigation :posts="posts" />
    <h1 class="title">This is a test</h1>
    <ul>
      <li v-for="(listItem, index) in listItems" :key="index">
        {{ listItem }}
      </li>
    </ul>
  </article>
</template>

<style>
article {
  font-family: sans-serif;
}
.title {
  color: red;
}
body {
  background: red;
}
</style>

<script>
import Navigation from "./_includes/Navigation.vue";
export default {
  data() {
    return {
      title: "Wow I'm So Excited To Use Vue In My Templates!",
      listItems: [
        "This is the first item",
        "This is the second",
        "This is perhaps the third, though who could truly say.",
      ],
    };
  },
  components: {
    Navigation,
  },
};
</script>
