<template>
<section class="home-main">
<div class="container">
  <_contentWrapper>
  <h3 class="subtitle" > {{ subtitle }}</h3>
    <h1 class="title"> {{ title }}</h1>
    <p class="text">
     {{ text }}
    </p>
    <div class="buttons">
      <TheButton> Get started </TheButton>
      <the-button  :light="true"> Catalog </the-button>
    </div>
  </_contentWrapper>
    <div class="banner">
      <img :src="banner_image" alt="">
    </div>
    <div class="home-socials">
      <ul>
        <li v-for="social in social_array" :key="social.icon">
          <a :href="social.link"> <i :class="social.icon"></i></a>
        </li>
      </ul>
    </div>
  </div>




</section>
</template>

<script>
import social_array from "@/frags/social_array";
import TheButton from "@/laylouts/TheButton";
import TheTitle from "@/laylouts/The-title";
import _contentWrapper from "@/views/home/components/_content-wrapper";
export default {
  name: "Main",
  components: {TheTitle, TheButton, _contentWrapper},

  data() {
    return{
      subtitle: 'Get Started',
      title : 'Get Started &' +
          '      Work with Us.',
      text:' When, while lovely valley teems with vapour around meand meridiansun strikes the upper impenetrable .\n' +
          '      foliage of my trees, and but a  thousand.' +
          '    ong the tall grass by the trickling stream; and, as I l',
      banner_image: require('@/images/sections/1img.png'),
      social_array: social_array
    }
  }
}
</script>

<style scoped lang="scss">
@import "../styles/main-section.scss";
</style>