<script setup>
const props = defineProps({
  infos: Object,
})
</script>

<template>
  <div :style="{ backgroundImage: `url(${infos.image})` }" class="container">
    <div>
      <h3>
        <span>{{ infos.category.toUpperCase() }}</span
        ><span>{{ infos.subCategory.toUpperCase() }}</span>
      </h3>
      <h1>
        <span>{{ infos.title }}</span>
      </h1>
    </div>
    <p>{{ infos.teaser }}</p>
  </div>
</template>

<style scoped>
.container {
  height: 550px;
  background-repeat: no-repeat;
  background-position: bottom;
  padding: 100px;
}

.container > div {
  position: relative;
}

.container > div::before {
  content: '';
  position: absolute;
  top: 0px;
  left: -5px;
  width: 5px;
  height: 100%;
  background: linear-gradient(#be80ff, #6325ff);
}

div h1 {
  font-family: Merriweather, serif;
  color: white;
  font-size: 32px;
  line-height: 46px;
  width: 750px;
  margin-bottom: 30px;
}

h1 span {
  background-color: black;
  padding: 5px;
}

h3 {
  font-size: 12px;
  line-height: 24px;
  color: white;
  background-color: black;
  display: inline;
  padding: 5px 0;
}

h3 span:first-child {
  background: linear-gradient(45deg, #be80ff, #6325ff);
  background-clip: text;
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  letter-spacing: 0.7px;
}

h3 span:last-child {
  padding: 0 10px;
  letter-spacing: 0.3px;
}

p {
  color: white;
  font-weight: 300px;
  line-height: 22px;
  width: 800px;
  font-size: 14px;
  background-color: rgba(0, 0, 0, 0.42);
  padding: 25px;
}
</style>
