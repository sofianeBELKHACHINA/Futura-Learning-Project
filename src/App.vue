<script setup>
import Header from './components/Header.vue'
import FrontPage from './components/FrontPage.vue'
import ArticleCard from './components/ArticleCard.vue'
import Footer from './components/Footer.vue'
import data from './assets/articles.json'
</script>

<template>
  <Header />
  <main>
    <FrontPage :infos="data.frontPage" />

    <div class="articlesList">
      <ArticleCard
        v-for="articleInfos in data.articlesList"
        :key="articleInfos.id"
        :articleInfos="articleInfos"
      />
    </div>
  </main>
  <Footer />
</template>

<style scoped>
main {
  padding: 50px 0;
}

.articlesList {
  /* border: solid 1px red; */
  padding: 50px 20px;
  display: flex;
  flex-wrap: wrap;
  gap: 30px;
}
</style>
