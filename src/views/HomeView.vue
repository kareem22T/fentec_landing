<template>
  <section class="hero">
    <div class="container">
      <div class="text">
        <h2>
          <span class="highlited">
            Fentec Algiria
          </span> is app for <br>
          renting scooters to get your <br>
          destiny fast, eco friendly
        </h2>
        <div class="btns">
          <a href=""><img src="/imgs/app.png" alt="App store"></a>
          <a href=""><img src="/imgs/play_store.png" alt="Play store"></a>
        </div>
      </div>
      <div class="img">
        <img src="/imgs/hero.png" alt="imgs from the app">
      </div>
    </div>
  </section>
  <div class="swiper-container">
    <div class="swiper-wrapper">
      <div
        v-for="(item, index) in items"
        :key="index"
        :class="{ 'main': index === activeSlideIndex, 'secondary': index !== activeSlideIndex }"
        class="swiper-slide"
      >
        {{ item }}
      </div>
    </div>
  </div>
  <section class="slider">
    <div class="container">
      <swiper
      :loop="true"
      :slidesPerView="5"
      :spaceBetween="30"
      :modules="modules"
      :navigation="true"
      :allowTouchMove="false"
      :breackpoints="{
        992 :{
          spaceBetween: 25
        },
      }"
      @slideChangeTransition="addChangesClass()"
      @slideChange="addChangesClass()"
      @slideChangeTransitionEnd="addChangesClass()"
      class="mySwiper"
    >
        <swiper-slide>
          <img src="/imgs/slider-1.png">
        </swiper-slide>
        <swiper-slide>
          <img src="/imgs/slider-2.png">
        </swiper-slide>
        <swiper-slide>
          <img src="/imgs/slider-3.png">
        </swiper-slide>
        <swiper-slide>
          <img src="/imgs/slider-4.png">
        </swiper-slide>
        <swiper-slide>
          <img src="/imgs/slider-5.png">
        </swiper-slide>
        <swiper-slide>
          <img src="/imgs/slider-1.png">
        </swiper-slide>
        <swiper-slide>
          <img src="/imgs/slider-2.png">
        </swiper-slide>
        <swiper-slide>
          <img src="/imgs/slider-3.png">
        </swiper-slide>
        <swiper-slide>
          <img src="/imgs/slider-4.png">
        </swiper-slide>
        <swiper-slide>
          <img src="/imgs/slider-5.png">
        </swiper-slide>
      </swiper>
    </div>
  </section>
  <section class="slider-mobile">
    <div class="container">
      <swiper
      :loop="true"
      :slidesPerView="3"
      :spaceBetween="30"
      :modules="modules"
      :navigation="true"
      :allowTouchMove="false"
      @slideChangeTransition="addChangesClassMobile()"
      @slideChange="addChangesClassMobile()"
      @slideChangeTransitionEnd="addChangesClassMobile()"
      class="mySwiper"
    >
        <swiper-slide>
          <img src="/imgs/slider-1.png">
        </swiper-slide>
        <swiper-slide>
          <img src="/imgs/slider-2.png">
        </swiper-slide>
        <swiper-slide>
          <img src="/imgs/slider-3.png">
        </swiper-slide>
        <swiper-slide>
          <img src="/imgs/slider-4.png">
        </swiper-slide>
        <swiper-slide>
          <img src="/imgs/slider-5.png">
        </swiper-slide>
        <swiper-slide>
          <img src="/imgs/slider-1.png">
        </swiper-slide>
        <swiper-slide>
          <img src="/imgs/slider-2.png">
        </swiper-slide>
        <swiper-slide>
          <img src="/imgs/slider-3.png">
        </swiper-slide>
        <swiper-slide>
          <img src="/imgs/slider-4.png">
        </swiper-slide>
        <swiper-slide>
          <img src="/imgs/slider-5.png">
        </swiper-slide>
      </swiper>
    </div>
  </section>
  <section class="vedio">
    <div class="container">

      <h2>How to enjoy the scooter </h2>
      <iframe width="560" height="315" src="https://www.youtube.com/embed/J3mpF2jkQ4vc?si=RxSieSTr_9RYS5ob" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>
    </div>
  </section>
  <section class="join_us">
    <h2>Join us!</h2>
    <div class="container">
      <div>
        <img src="/imgs/join-us-1.png">
        <button>
          As point seller
        </button>
      </div>
      <div>
        <img src="/imgs/join-us-2.png">
        <button>
          As accountant
        </button>
      </div>
      <div>
        <img src="/imgs/join-us-3.png">
        <button>
          As technican
        </button>
      </div>
    </div>
  </section>
  <footer>
      <div class="content">
        <a href="">
          Terms and conditions<br>
          Service agreement<br>
          Privacy police
        </a>
        <div class="btns">
          <a href=""><img src="/imgs/app.png" alt="App store"></a>
          <a href=""><img src="/imgs/play_store.png" alt="Play store"></a>
        </div>
      </div>
      <div class="img">
        <img src="/imgs/footer-img.png" alt="">
        <p>Get fast, safe and enjoy</p>
      </div>
  </footer>
</template>

<script>
  global.jQuery = require('jquery');
  var $ = global.jQuery;
  window.$ = $;
  // Import Swiper Vue.js components
  import { Swiper, SwiperSlide } from 'swiper/vue';

  // Import Swiper styles
  import 'swiper/css';

  import 'swiper/css/pagination';

  // import required modules
  import { Pagination, Navigation } from 'swiper/modules';
  import 'swiper/css/navigation';


export default {
  name: 'HomeView',
  components: {
      Swiper,
      SwiperSlide,
    },
    setup() {
      return {
        modules: [Pagination, Navigation],
      };
    },
    methods: {
      addChangesClass() {
        $(".swiper-slide-active").next().next().addClass("main")
        $(".swiper-slide-active").next().next().siblings().removeClass("main")
          $(".swiper-slide").removeClass("secondary")
          $(".swiper-slide-active").next().addClass("secondary")
        $(".swiper-slide-active").next().next().next().addClass("secondary")
      },
      addChangesClassMobile() {
          $(".swiper-slide-active").next().addClass("main")
        $(".swiper-slide-active").next().siblings().removeClass("main")
      },
    },
}
</script>
