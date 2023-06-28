<script>
export default {
  data() {
    return {
      image: 'hero.jpg',
    };
  },
  methods: {
    getImagePath(image) {
      return new URL(`../assets/${image}`, import.meta.url).href;
    }
  }
};
</script>

<template>
  <img :src="getImagePath(image)" alt="Hero">
</template>

<style scoped>
img {
  height: 700px;
  width: 100%;
}
</style>