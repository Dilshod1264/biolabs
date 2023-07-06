<template>
<section class="home-partners">

  <the-title  :sub="sub" :title="title"/>

  <div class="slider">
    <!-- Swiper -->
    <swiper ref="mySwiper" :options="swiperOptions">
      <swiper-slide v-for="img   in images_array" :key="img">
        <img :src="img" alt="brands ">
      </swiper-slide>

    </swiper>
    <swiper class="swiper-l-r">
      <div class="swiper-pagination" slot="pagination"></div>
    </swiper>

  </div>
</section>
</template>

<script>

import TheTitle from "@/laylouts/The-title";
//swiper import
import { Swiper, SwiperSlide } from 'vue-awesome-swiper'
import 'swiper/css/swiper.css'

export default {
  name: "HomePartners",
  components: {
    TheTitle,Swiper, SwiperSlide },

  data() {
    return {
      sub: 'Partners',
      title: 'Our new partner',
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
      images_array:[
          require('../../../images/sections/img2.png'),
        require('../../../images/sections/img3.png'),
        require('../../../images/sections/img4.png'),
        require('../../../images/sections/img5.png'),

      ]
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
@import "../styles/homepartners.scss";


</style>