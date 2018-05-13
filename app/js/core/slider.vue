<template>
  <section :class="[cName]">
    <swiper :options="options" :not-next-tick="options.notNextTick">
        <swiper-slide v-for="item in items" :key="item.href">
          <router-link to="item.href">
            <img :src="item.src" alt="">
          </router-link>
        </swiper-slide>
    </swiper>
  </section>
</template>

<script>
import { swiper, swiperSlide } from "vue-awesome-swiper";
export default {
  props: {
    cName: {
      type: String,
      default: ""
    },
    options: {
      type: Object,
      default() {
        return {
          autoplay: true,
          notNextTick: true,
          loop: true,
          pagination: {
            el: ".swiper-pagination"
          }
        };
      }
    },
    items: {
      type: Array,
      default() {
        return [];
      }
    }
  },

  components: {
    swiper,
    swiperSlide
  }
};
</script>

<style lang="scss" scoped>
@import "~swiper/dist/css/swiper.css";
</style>


