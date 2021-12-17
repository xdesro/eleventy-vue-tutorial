<template>
  <article>
    <Navigation :posts="posts" />
    <h1>This is a test</h1>
    <ul>
      <li v-for="(listItem, index) in listItems" :key="index">
        {{ listItem }}
      </li>
    </ul>
  </article>
</template>

<style>
body {
  background-color: #efefef;
}
article {
  font-family: sans-serif;
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
