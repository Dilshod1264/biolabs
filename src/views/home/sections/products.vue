<template>
  <section class="products">

<div class="container">
  <the-title  :sub="sub" :title="title"/>

  <div class="slider">
    <!-- Swiper -->
    <swiper ref="mySwiper" :options="swiperOptions">
      <swiper-slide v-for="product  in product" :key="products">
        <div class="blok">
          <img :src="product.img" alt="">
          <div class="text-blok">
            <h5>{{ product.text }}</h5>
            <p>{{ product.id }}</p>
            <h6><del> {{ product.old_price }} </del></h6>
            <div class="buy">
              <h1>{{ product.new_price }}</h1>
              <i :class="product.icons"></i>
            </div>
          </div>
        </div>

      </swiper-slide>

      <div class="swiper-pagination" slot="pagination"></div>
    </swiper>
<!--    <swiper class="swiper-l-r">-->
<!--      <div class="swiper-pagination" slot="pagination"></div>-->
<!--    </swiper>-->

  </div>
</div>
  </section>
</template>

<script>

import TheTitle from "@/laylouts/The-title";
//swiper import
import { Swiper, SwiperSlide } from 'vue-awesome-swiper'
import 'swiper/css/swiper.css'
import product from "@/frags/product";
export default {
  components: {
    TheTitle,Swiper, SwiperSlide },

  data() {
    return {
      sub: 'Our Products',
      title: 'Top products that have won the hearts of our customers',
      swiperOptions:{
        pagination: {
          el: '.swiper-pagination'
        },
        slidesPerView: 4,
        loop: true,
        speed: 5000,
        autoplay: { delay: 0},
        breakpoints: {
          0: {
            slidesPerView: 1,
            spaceBetween: 20
          },
          731:{
            slidesPerView: 2,
            spaceBetween: 20
          },
          971:{
            slidesPerView: 3,
            spaceBetween: 20
          },
          1681:{
            slidesPerView: 4,
            spaceBetween: 20
          },

        }
      },

      product:product

    }
  },
  methods: {
    // ...mapActions(['getPartners'])
  },
  computed: {
    // ...mapGetters(["partners_list"])

  },
  mounted() {
// this.getPartners();

  }


}

</script>

<style scoped lang="scss">
@import "../styles/product.scss";
</style>