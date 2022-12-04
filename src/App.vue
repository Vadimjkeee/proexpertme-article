<template>
  <div class="app">
    <section-article :title="title" :list="list" />
  </div>
</template>

<script>
import sectionArticle from "@/components/sectionArticle";
export default {
  components: {
    sectionArticle,
  },
  data() {
    return {
      title: "О марке",
      list: [
        {
          title: "lA ROCHE-POSAY БРЕНД №1 ПО РЕКОМЕНДАЦИИ ДЕРМАТОЛОГОВ",
          image: { src: require("@/assets/img/doctor.png"), alt: "Доктор" },
          subtitle:
            "Бренд La Roche-Posay сотрудничает с дерматологами на всех этапах, начиная с разработки. Мы создаём средства с эффективной концентрацией активных ингредиентов, которые подойдут даже для чувствительной кожи.",
          text: "Подробнее",
          icon: { src: require("@/assets/img/arrow.svg"), alt: "Стрелка" },
        },

        {
          title: "ЭКСПЕРТ В ОБЛАСТИ МИКРОБИОМА КОЖИ",
          image: { src: require("@/assets/img/microbiome.png"), alt: "Микробиом" },
          subtitle:
            "Знания, полученные за 9 лет изучения микробиома кожи, вдохновляют La Roche-Posay на создание инновационных косметических средств с доказанной эффективностью.",
          text: "Подробнее",
          icon: { src: require("@/assets/img/arrow.svg"), alt: "Стрелка" },
        },
        {
          title: "ИННОВАЦИОННЫЙ СЕРВИС",
          image: { src: require("@/assets/img/diagnostics.png"), alt: "Диагностика" },
          subtitle: "Онлайн-диагностика проблемной кожи.",
          text: "Подробнее",
          icon: { src: require("@/assets/img/arrow.svg"), alt: "Стрелка" },
        },
        {
          title:
            "БЕЗОПАСНОСТЬ И ОПТИМАЛЬНАЯ ПЕРЕНОСИМОСТЬ. ЭФФЕКТИВНАЯ КОНЦЕНТРАЦИЯ ИНГРЕДИЕНТОВ",
          image: { src: require("@/assets/img/safety.png"), alt: "Лицо женщины" },
          subtitle:
            "Все, что вы хотели знать об ингредиентах. Ваша безопасность — наш абсолютный приоритет",
          text: "Подробнее",
          icon: { src: require("@/assets/img/arrow.svg"), alt: "Стрелка" },
          width: true,
        },
      ],
    };
  },
};
</script>

<style>
</style>