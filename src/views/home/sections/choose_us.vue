<template>
<section class="choose-section">
  <div class="container">
   <div class="main">
     <div class="choose_title">
       <h3 class="sub">{{ sub}}</h3>
       <h1 class="title"> {{ title }} </h1>
       <p>We are idea generators, goal seekers, challenge-thirsty professionals, creators of <br> unique Internet projects. We deliver unconventional solutions
         <br>
         each project is a meaningful adventure
         , in which we become partners with our clients, on the road to perfection. </p>
       <TheButton>Show more...</TheButton>
     </div>
     <div class="choose-banner">
    <div class="img">
      <img src="../../../images/sections/choose.png" alt="">
      <img src="../../../images/sections/choose2.png" alt="">
    </div>
     </div>
   </div>
  </div>
</section>
</template>

<script>


import TheButton from "@/laylouts/TheButton";
export default {
  name: "choose_us",
  components: {
    TheButton,

  },
  data() {
    return{
      sub: 'Why choose us',

       til: {
         en: 'About us',
         ru: 'О нас',
         uz: 'Biz haqimizda',

       },

      title: 'An Exceptionally Unique Experience Tailored To You'
    }
  }
}
</script>

<style scoped lang="scss">
@import "../styles/choose.scss";
</style>