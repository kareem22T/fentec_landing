<template>
  <section class="hero">
    <div class="container">
      <div class="text">
        <h2>
          <span class="highlited">
            Fentec Mobility
          </span> is the first eco-friendly transportation  company in Algeria <br /> and The Arab Maghreb <span class="highlited Click-here" style="cursor: pointer;" @click="showPopup = !showPopup"><u>More</u></span>
        </h2>
        <div class="btns">
          <a href=""><img src="/imgs/app.png?v=1.0" alt="App store"></a>
          <a href=""><img src="/imgs/play_store.png?v=1.0" alt="Play store"></a>
        </div>
      </div>
      <div class="img">
        <img src="/imgs/hero.png?v=1.0" alt="imgs from the app">
      </div>
    </div>
  </section>
  <div @click="showPopup = false" class="hide-content" v-if="showPopup"></div>
  <div class="more-pop-up" v-if="showPopup">
      <svg @click="showPopup = false" xmlns="http://www.w3.org/2000/svg" class="icon icon-tabler icon-tabler-square-x" width="20" height="20" viewBox="0 0 24 24" stroke-width="1.5" stroke="#000000" fill="none" stroke-linecap="round" stroke-linejoin="round">
        <path stroke="none" d="M0 0h24v24H0z" fill="none"/>
        <path d="M3 5a2 2 0 0 1 2 -2h14a2 2 0 0 1 2 2v14a2 2 0 0 1 -2 2h-14a2 2 0 0 1 -2 -2v-14z" />
        <path d="M9 9l6 6m0 -6l-6 6" />
      </svg>
      <div class="content">
        The problem of traffic jams, fuel costs, air and noise pollution have necessitated us thinking to find solutions. <br>
        Fentec Mobility is the first integrated system offering shared electric vehicles in Algeria and The Arab Maghreb.  <br>
        We aim to transform the current mode of transportation in the cities to an enjoyable, safe, sustainable, eco-friendly, shareable and affordable mode. <br>
        We are on a mission to replace all car trips in cities and Universities under 15km. <br>
        Safety First, The helmet is available for all our vehicles. <br>
        With an easy-to-use mobile app and a team of experts available at any time for a better experience.
      </div>
      <div class="content-2">
        Fentec Mobility Your Solution <br>
        to a Green and Sustainable Future.
      </div>
      <img src="/imgs/message.png" class="message">
      <img src="/imgs/popup-photo.png" class="popup-img">
      <div class="btns">
        <a href=""><img src="/imgs/app.png?v=1.0" alt="App store"></a>
        <a href=""><img src="/imgs/play_store.png?v=1.0" alt="Play store"></a>
      </div>
  </div> 
  <section class="social">
    <h1>Follow us</h1>
    <div class="links">
      <a href="">
        <svg xmlns="http://www.w3.org/2000/svg" class="icon icon-tabler icon-tabler-brand-youtube" width="44" height="44" viewBox="0 0 24 24" stroke-width="1.5" stroke="#2c3e50" fill="none" stroke-linecap="round" stroke-linejoin="round">
          <path stroke="none" d="M0 0h24v24H0z" fill="none"/>
          <path d="M2 8a4 4 0 0 1 4 -4h12a4 4 0 0 1 4 4v8a4 4 0 0 1 -4 4h-12a4 4 0 0 1 -4 -4v-8z" />
          <path d="M10 9l5 3l-5 3z" />
        </svg>
      </a>
      <a href="">
        <svg xmlns="http://www.w3.org/2000/svg" class="icon icon-tabler icon-tabler-brand-facebook" width="44" height="44" viewBox="0 0 24 24" stroke-width="1.5" stroke="#2c3e50" fill="none" stroke-linecap="round" stroke-linejoin="round">
          <path stroke="none" d="M0 0h24v24H0z" fill="none"/>
          <path d="M7 10v4h3v7h4v-7h3l1 -4h-4v-2a1 1 0 0 1 1 -1h3v-4h-3a5 5 0 0 0 -5 5v2h-3" />
        </svg>
      </a>
      <a href="">
        <svg xmlns="http://www.w3.org/2000/svg" class="icon icon-tabler icon-tabler-brand-whatsapp" width="44" height="44" viewBox="0 0 24 24" stroke-width="1.5" stroke="#2c3e50" fill="none" stroke-linecap="round" stroke-linejoin="round">
          <path stroke="none" d="M0 0h24v24H0z" fill="none"/>
          <path d="M3 21l1.65 -3.8a9 9 0 1 1 3.4 2.9l-5.05 .9" />
          <path d="M9 10a.5 .5 0 0 0 1 0v-1a.5 .5 0 0 0 -1 0v1a5 5 0 0 0 5 5h1a.5 .5 0 0 0 0 -1h-1a.5 .5 0 0 0 0 1" />
        </svg>
      </a>
      <a href="">
        <svg xmlns="http://www.w3.org/2000/svg" class="icon icon-tabler icon-tabler-brand-tiktok" width="44" height="44" viewBox="0 0 24 24" stroke-width="1.5" stroke="#2c3e50" fill="none" stroke-linecap="round" stroke-linejoin="round">
          <path stroke="none" d="M0 0h24v24H0z" fill="none"/>
          <path d="M21 7.917v4.034a9.948 9.948 0 0 1 -5 -1.951v4.5a6.5 6.5 0 1 1 -8 -6.326v4.326a2.5 2.5 0 1 0 4 2v-11.5h4.083a6.005 6.005 0 0 0 4.917 4.917z" />
        </svg>
      </a>
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
          <img src="/imgs/slider-6.png?v=1.0">
        </swiper-slide>

        <swiper-slide>
          <img src="/imgs/slider-4.png?v=1.0">
        </swiper-slide>
        <swiper-slide>
          <img src="/imgs/slider-3.png?v=1.0">
        </swiper-slide>
        <swiper-slide>
          <img src="/imgs/slider-2.png?v=1.0">
        </swiper-slide>
        <swiper-slide>
          <img src="/imgs/slider-5.png?v=1.0">
        </swiper-slide>
        <swiper-slide>
          <img src="/imgs/slider-1.png?v=1.0">
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
          <img src="/imgs/slider-6.png?v=1.0">
        </swiper-slide>

        <swiper-slide>
          <img src="/imgs/slider-3.png?v=1.0">
        </swiper-slide>
        <swiper-slide>
          <img src="/imgs/slider-4.png?v=1.0">
        </swiper-slide>
        <swiper-slide>
          <img src="/imgs/slider-2.png?v=1.0">
        </swiper-slide>
        <swiper-slide>
          <img src="/imgs/slider-5.png?v=1.0">
        </swiper-slide>
        <swiper-slide>
          <img src="/imgs/slider-1.png?v=1.0">
        </swiper-slide>
      </swiper>
    </div>
  </section>
  <section class="cumming_sonn">
    <div class="container">
      <h2>Coming soon, stay tuned!</h2>
      <p>The first complete eco-friendly transportation system in Algeria and The Arab-Maghreb. 
      <br /> Made by ALGERIANS.</p>
      <img src="/imgs/Coming.png?v=1.0" alt="">
    </div>
  </section>
  <!-- <section class="vedio">
    <div class="container">

      <h2>How to enjoy the scooter </h2>
      <iframe width="560" height="315" src="https://www.youtube.com/embed/J3mpF2jkQ4vc?si=RxSieSTr_9RYS5ob" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>
    </div>
  </section> -->
  <section class="join_us">
    <h2>Join us!</h2>
    <div class="container">
      <div>
        <img src="/imgs/join-us-1.png?v=1.0">
        <button>
          As Point Seller
        </button>
      </div>
      <div>
        <img src="/imgs/join-us-2.png?v=1.0">
        <button>
          As Accountant
        </button>
      </div>
      <div>
        <img src="/imgs/join-us-3.png?v=1.0">
        <button>
          As Technician
        </button>
      </div>
    </div>
  </section>
  <footer>
      <div class="content">
        <p style="color: #ffe5cf;margin-bottom: -10px;" class="mobile-footer-paragraoh">Go safely, Freely and Enjoyably <br/>
          <span style="font-size: 14px;">Together Towards a Sustainable World.</span>
        </p>

        <a href="">
          Terms and conditions<br>
          Service agreement<br>
          Privacy police
        </a>
        <div class="links">
          <a href="">
            <svg xmlns="http://www.w3.org/2000/svg" class="icon icon-tabler icon-tabler-brand-youtube" width="44" height="44" viewBox="0 0 24 24" stroke-width="1.5" stroke="#2c3e50" fill="none" stroke-linecap="round" stroke-linejoin="round">
              <path stroke="none" d="M0 0h24v24H0z" fill="none"/>
              <path d="M2 8a4 4 0 0 1 4 -4h12a4 4 0 0 1 4 4v8a4 4 0 0 1 -4 4h-12a4 4 0 0 1 -4 -4v-8z" />
              <path d="M10 9l5 3l-5 3z" />
            </svg>
          </a>
          <a href="">
            <svg xmlns="http://www.w3.org/2000/svg" class="icon icon-tabler icon-tabler-brand-facebook" width="44" height="44" viewBox="0 0 24 24" stroke-width="1.5" stroke="#2c3e50" fill="none" stroke-linecap="round" stroke-linejoin="round">
              <path stroke="none" d="M0 0h24v24H0z" fill="none"/>
              <path d="M7 10v4h3v7h4v-7h3l1 -4h-4v-2a1 1 0 0 1 1 -1h3v-4h-3a5 5 0 0 0 -5 5v2h-3" />
            </svg>
          </a>
          <a href="">
            <svg xmlns="http://www.w3.org/2000/svg" class="icon icon-tabler icon-tabler-brand-whatsapp" width="44" height="44" viewBox="0 0 24 24" stroke-width="1.5" stroke="#2c3e50" fill="none" stroke-linecap="round" stroke-linejoin="round">
              <path stroke="none" d="M0 0h24v24H0z" fill="none"/>
              <path d="M3 21l1.65 -3.8a9 9 0 1 1 3.4 2.9l-5.05 .9" />
              <path d="M9 10a.5 .5 0 0 0 1 0v-1a.5 .5 0 0 0 -1 0v1a5 5 0 0 0 5 5h1a.5 .5 0 0 0 0 -1h-1a.5 .5 0 0 0 0 1" />
            </svg>
          </a>
          <a href="">
            <svg xmlns="http://www.w3.org/2000/svg" class="icon icon-tabler icon-tabler-brand-tiktok" width="44" height="44" viewBox="0 0 24 24" stroke-width="1.5" stroke="#2c3e50" fill="none" stroke-linecap="round" stroke-linejoin="round">
              <path stroke="none" d="M0 0h24v24H0z" fill="none"/>
              <path d="M21 7.917v4.034a9.948 9.948 0 0 1 -5 -1.951v4.5a6.5 6.5 0 1 1 -8 -6.326v4.326a2.5 2.5 0 1 0 4 2v-11.5h4.083a6.005 6.005 0 0 0 4.917 4.917z" />
            </svg>
          </a>
        </div>
        <div class="btns">
          <a href=""><img src="/imgs/app.png?v=1.0" alt="App store"></a>
          <a href="http://fentecmobility.com/fentec.apk" download ><img src="/imgs/play_store.png?v=1.0" alt="Play store"></a>
        </div>
      </div>
      <div class="img">
        <img src="/imgs/footer-img.png?v=1.0" alt="">
        <p>Go safely, Freely and Enjoyably <br/>
          <span style="font-size: 16px;">Together Towards a Sustainable World.</span>
        </p>
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
    data() {
      return {
          showPopup: false
      }
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
