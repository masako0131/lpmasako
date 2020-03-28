<template>
  <div>
    <section class="menu cid-rTiAafnmIP" once="menu" id="menu1-c">
      <nav class="navbar navbar-expand beta-menu navbar-dropdown align-items-center navbar-fixed-top navbar-toggleable-sm bg-color">
        <button class="navbar-toggler navbar-toggler-right" type="button" data-toggle="collapse" data-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
          <div class="hamburger">
            <span></span>
            <span></span>
            <span></span>
            <span></span>
          </div>
        </button>
        <div class="menu-logo">
          <div class="navbar-brand">
            <span class="navbar-logo">
              <nuxt-link :to="localePath('index', $i18n.locale)">
                <img src="/mobiris_assets/images/logo_nav.png"  style="height: 2.8rem;">
              </nuxt-link>
            </span>
            <!-- <span class="navbar-caption-wrap">
              <nuxt-link class="navbar-caption text-warning display-4" :to="localePath('index', $i18n.locale)">
                La Pâtisserie Masako
              </nuxt-link>
            </span> -->
          </div>
        </div>
        <div class="collapse navbar-collapse" id="navbarSupportedContent">
          <ul class="navbar-nav nav-dropdown nav-right" data-app-modern-menu="true">
            <li class="nav-item">
              <a class="nav-link link text-warning display-4" href="#content5-o">
                <!-- <span class="mbri-home mbr-iconfont mbr-iconfont-btn"></span> -->
                {{ $t('products') }}
              </a>
            </li>
            <li class="nav-item">
              <a class="nav-link link text-warning display-4" href="#testimonials3-7">
                <!-- <span class="mbri-info mbr-iconfont mbr-iconfont-btn"></span> -->
                {{ $t('about') }}
              </a>
            </li>
            <li class="nav-item">
              <nuxt-link v-if="$i18n.locale === 'zh'" class="nav-link link text-warning display-4" :to="switchLocalePath('ja')">日本語</nuxt-link>
              <nuxt-link v-if="$i18n.locale === 'ja'" class="nav-link link text-warning display-4" :to="switchLocalePath('zh')">繁體中文</nuxt-link>
            </li>
          </ul>
        </div>
      </nav>
    </section>

  <nuxt />


  <!-- <script src="/mobiris_assets/web/assets/jquery/jquery.min.js"></script> -->
  <!-- <script src="/mobiris_assets/popper/popper.min.js"></script> -->
  <!-- <script src="/mobiris_assets/bootstrap/js/bootstrap.min.js"></script> -->
  <!-- <script src="/mobiris_assets/smoothscroll/smooth-scroll.js"></script>
  <script src="/mobiris_assets/dropdown/js/nav-dropdown.js"></script>
  <script src="/mobiris_assets/dropdown/js/navbar-dropdown.js"></script>
  <script src="/mobiris_assets/touchswipe/jquery.touch-swipe.min.js"></script>
  <script src="/mobiris_assets/tether/tether.min.js"></script> -->
  <!-- <script src="/mobiris_assets/vimeoplayer/jquery.mb.vimeo_player.js"></script>
  <script src="/mobiris_assets/parallax/jarallax.min.js"></script>
  <script src="/mobiris_assets/masonry/masonry.pkgd.min.js"></script>
  <script src="/mobiris_assets/imagesloaded/imagesloaded.pkgd.min.js"></script>
  <script src="/mobiris_assets/bootstrapcarouselswipe/bootstrap-carousel-swipe.js"></script>
  <script src="/mobiris_assets/ytplayer/jquery.mb.ytplayer.min.js"></script> -->
  <!-- <script src="/mobiris_assets/theme/js/script.js"></script> -->
  <!-- <script src="/mobiris_assets/gallery/player.min.js"></script>
  <script src="/mobiris_assets/gallery/script.js"></script>
  <script src="/mobiris_assets/slidervideo/script.js"></script> -->

  </div>
  
</template>



<script>
export default {
  head() {
    const i18nSeo = this.$nuxtI18nSeo();
    return {
      titleTemplate: "%s - La Pâtisserie Masako",
      htmlAttrs: {
        ...i18nSeo.htmlAttrs
      },
      meta: [...i18nSeo.meta],
      script: [
        {
          src: "/mobiris_assets/web/assets/jquery/jquery.min.js"
        },
        {
          src: "/mobiris_assets/popper/popper.min.js"
        },
        {
          src: "/mobiris_assets/bootstrap/js/bootstrap.min.js"
        },
        {
          src: "/mobiris_assets/smoothscroll/smooth-scroll.js"
        },
        {
          src: "/mobiris_assets/dropdown/js/nav-dropdown.js"
        },
        {
          src: "/mobiris_assets/dropdown/js/navbar-dropdown.js"
        },
        {
          src: "/mobiris_assets/touchswipe/jquery.touch-swipe.min.js"
        },
        {
          src: "/mobiris_assets/tether/tether.min.js"
        },
        {
          src: "/mobiris_assets/vimeoplayer/jquery.mb.vimeo_player.js"
        },
        {
          src: "/mobiris_assets/parallax/jarallax.min.js"
        },
        {
          src: "/mobiris_assets/masonry/masonry.pkgd.min.js"
        },
        {
          src: "/mobiris_assets/imagesloaded/imagesloaded.pkgd.min.js"
        },
        {
          src: "/mobiris_assets/ytplayer/jquery.mb.ytplayer.min.js"
        },
        // {
        //   src: "/mobiris_assets/bootstrapcarouselswipe/bootstrap-carousel-swipe.js", defer: true
        // },
        // {
        //   src: "/mobiris_assets/theme/js/script.js", defer: true
        // },
        // {
        //   src: "/mobiris_assets/gallery/player.min.js", defer: true
        // },
        // {
        //   src: "/mobiris_assets/gallery/script.js", defer: true
        // },
        // {
        //   src: "/mobiris_assets/slidervideo/script.js", defer: true
        // }
      ],
      link: [
        {
          rel: "stylesheet",
          href: "/mobiris_assets/web/assets/mobirise-icons/mobirise-icons.css"
        },
        {
          rel: "stylesheet",
          href: "/mobiris_assets/bootstrap/css/bootstrap.min.css"
        },
        {
          rel: "stylesheet",
          href: "/mobiris_assets/bootstrap/css/bootstrap-grid.min.css"
        },
        {
          rel: "stylesheet",
          href: "/mobiris_assets/bootstrap/css/bootstrap-reboot.min.css"
        },
        {
          rel: "stylesheet",
          href: "/mobiris_assets/dropdown/css/style.css"
        },
        {
          rel: "stylesheet",
          href: "/mobiris_assets/tether/tether.min.css"
        },
        {
          rel: "stylesheet",
          href: "/mobiris_assets/theme/css/style.css"
        },
        {
          rel: "stylesheet",
          href: "/mobiris_assets/gallery/style.css"
        },
        {
          rel: "preload",
          href: "/mobiris_assets/mobirise/css/mbr-additional.css"
        },
        {
          rel: "stylesheet",
          href: "/mobiris_assets/mobirise/css/mbr-additional.css"
        },
        {
          rel: "stylesheet",
          href: "https://maxcdn.bootstrapcdn.com/font-awesome/4.7.0/css/font-awesome.min.css"
        },
        ...i18nSeo.link
      ]
    };
  },
  data() {
    return {
    };
  },
  watch: {
    
  },
  async mounted() {
   
  }
};
</script>
<style>
.page-enter-active,
.page-leave-active {
  transition: opacity 0.5s;
}
.page-enter,
.page-leave-active {
  opacity: 0;
}
</style>