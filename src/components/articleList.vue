<template>
  <div class="list">
    <article-item  :key="item.id" v-for="item in list" :item="item" />
  </div>
</template>
    
    <script>
import articleItem from "@/components/articleItem";
export default {
  props: {
    list: { type: Array },
  },
  components: { articleItem },
  data() {
    return {};
  },
};
</script>
    
<style scoped lang="scss">
.list {
  padding-bottom: 6rem;
}
</style>