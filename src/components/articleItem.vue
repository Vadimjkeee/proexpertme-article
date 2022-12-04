<template>
  <div class="section-item">
    <p class="title" :class="{ mod: item.width === true }">
      {{ item.title }}
    </p>
    <div class="image-wrapper">
      <img :src="item.image.src" :alt="item.image.alt" class="image" />
    </div>
    <p class="subtitle">{{ item.subtitle }}</p>
    <div class="more">
      <span class="more__text"> {{ item.text }}</span>
      <button type="submit" class="arrow">
        <img :src="item.icon.src" :alt="item.icon.alt" class="icon" />
      </button>
    </div>
  </div>
</template>
    
<script>
export default {
  props: {
    item: {
      title: { type: String, default: 'lA ROCHE-POSAY БРЕНД №1 ПО РЕКОМЕНДАЦИИ ДЕРМАТОЛОГОВ' },
      image: { type: Object, default: { src: require("@/assets/img/doctor.png"), alt: 'Доктор' }},
      subtitle: { type: String, default: 'Бренд La Roche-Posay сотрудничает с дерматологами на всех этапах, начиная с разработки. Мы создаём средства с эффективной концентрацией активных ингредиентов, которые подойдут даже для чувствительной кожи.' },
      text: { type: String, default: 'Подробнее' },
      icon: { type: Object, default: { src: require("@/assets/img/arrow.svg"), alt: 'Стрелка' }}
    },
  },
  data() {
    return {};
  },
};
</script>
      
<style scoped lang="scss">
@import "@/assets/scss/modules/mixins.scss";

.section-item{
  margin-bottom: 6rem;
}
.image-wrapper {
    margin-bottom: 3rem;
  }

.image {
    width: 100%;
  }

.title {
    font-family: "Montserrat Light";
    @include adaptiv-font(5, 3);
    line-height: 120%;
    text-transform: uppercase;
    color: #000000;
    margin-bottom: 4.5rem;
    max-width: 77rem;
  }
.subtitle {
    margin-bottom: 5rem;
    font-family: "Montserrat Light";
    @include adaptiv-font(2, 1.5);
    line-height: 150%;
    color: #000000;
  }
.more {
    display: flex;
    align-items: center;
    &__text {
        margin-right: 2rem;
        font-family: "Montserrat Bold";
        @include adaptiv-font(2.039, 1.5);
        line-height: 120%;
        color: #000000;
    }
}

.arrow{
    border: none;
    cursor: pointer;
    background-color: inherit;
}
.mod{
    max-width: 100%;
}
</style>