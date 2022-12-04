<template>
  <article class="section">
    <div class="container">
      <h1 class="section__title">{{ title }}</h1>
      <article-list :list='list' />
    </div>
  </article>
</template>
  
  <script>
import articleList from "@/components/articleList";
export default {
  props: {
    title: { type: String, default: "О марке" },
    list: { type: Array },
  },
  components: { articleList },
  data() {
    return {};
  },
};
</script>
  
<style scoped lang="scss">

@import '@/assets/scss/modules/mixins.scss';

.section {
  padding: 6rem 2rem 0;
    &__title {
        font-family: "Montserrat Bold";
        @include adaptiv-font(7, 4);
        line-height: 100%;
        color: #000000;
    }
}

.section .container{
  display: flex;
  flex-direction: column;
  row-gap: 6rem;
}
</style>