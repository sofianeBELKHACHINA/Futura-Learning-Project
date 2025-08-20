<script setup>
const props = defineProps({
  articleInfos: Object,
})
</script>

<template>
  <div>
    <img :src="articleInfos.image" alt="" />

    <p>
      <span>{{ articleInfos.category.toUpperCase() }}</span
      ><span>{{ articleInfos.subCategory.toUpperCase() }}</span>
    </p>

    <h2>{{ articleInfos.title }}</h2>
    <p class="date">{{ articleInfos.date }}</p>
  </div>
</template>

<style scoped>
div {
  width: calc((100% - 100px) / 4);
  height: 480px;
}

img {
  height: 300px;
  width: 100%;
  object-fit: cover;
  margin-bottom: 10px;
}

span {
  font-size: 12px;
}

span:first-child {
  font-weight: bold;
  background: linear-gradient(45deg, #be80ff, #6325ff);
  background-clip: text;
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  letter-spacing: 0.7px;
}

span:last-child {
  letter-spacing: 0.3px;
  font-weight: 300;
}

h2 {
  margin: 10px 0;
  font-size: 14px;
  font-weight: bold;
  line-height: 20px;
  font-family: Merriweather, serif;
}

.date {
  font-weight: 300;
  font-size: 12px;
  color: grey;
}
</style>
