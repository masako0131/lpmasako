<template>
  <div>
    <div id="fb-root"></div>
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
              <a class="nav-link link text-warning display-4" href="https://www.facebook.com/la.patisserie.masako/" target="_blank">
                <span class="socicon-facebook socicon text-warning"></span>
              </a>
            </li>
            <li class="nav-item">
              <a class="nav-link link text-warning display-4" href="https://www.instagram.com/patissiermasako" target="_blank">
                <span class="socicon-instagram socicon text-warning"></span>
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


  <section class="cid-rTiEqWMzJ1 mbr-reveal mbr-parallax-background" id="footer1-l" :style="{ backgroundImage: `url('')` }">
    <div class="mbr-overlay" style="opacity: 1; background-color: #513B58;"></div>
    <div class="container">
        <!-- <div class="media-container-row content text-white">
            <div class="col-12 col-md-3">
                <div class="media-wrap">
                    <nuxt-link :to="localePath('index', $i18n.locale)">
                      <img src="/mobiris_assets/images/logo.png" alt="">
                    </nuxt-link>
                </div>
            </div>
           
            <div class="col-12 col-md-4 mbr-fonts-style display-7">
                <h5 class="pb-3 text-warning">
                    Contacts
                </h5>
                <p class="mbr-text text-warning">
                    Email: <a href="mailto:la.patissier.masako@gmail.com">la.patissier.masako@gmail.com</a>
                </p>
            </div>
            <div class="col-12 col-md-4 mbr-fonts-style display-7">
                
            </div>
        </div> -->
        <div class="footer-lower">
            <!-- <div class="media-container-row">
                <div class="col-sm-12">
                    <hr>
                </div>
            </div> -->
            <div class="media-container-row mbr-white">
                <div class="col-sm-6 copyright">
                    <p class="mbr-text mbr-fonts-style display-7 text-warning">
                        © Copyright 2020 Hayashi Masako - All Rights Reserved
                    </p>
                </div>
                <div class="col-md-6">
                    <div class="social-list align-right">
                      <div class="soc-item">
                            <a href="mailto:la.patissier.masako@gmail.com" target="_blank">
                                <span class="socicon-mail socicon mbr-iconfont mbr-iconfont-social text-warning"></span>
                            </a>
                        </div>
                        <div class="soc-item">
                            <a href="https://m.me/la.patisserie.masako" target="_blank">
                                <span class="socicon-messenger socicon mbr-iconfont mbr-iconfont-social text-warning"></span>
                            </a>
                        </div>
                        <div class="soc-item">
                            <a href="https://www.instagram.com/patissiermasako" target="_blank">
                                <span class="socicon-instagram socicon mbr-iconfont mbr-iconfont-social text-warning"></span>
                            </a>
                        </div>
                        <div class="soc-item">
                            <a href="https://www.facebook.com/la.patisserie.masako/" target="_blank">
                                <span class="socicon-facebook socicon mbr-iconfont mbr-iconfont-social text-warning"></span>
                            </a>
                        </div>
                        <div class="soc-item">
                            <a href="https://www.youtube.com/channel/UCwqsitXmX-76-rEL9dRExGA" target="_blank">
                                <span class="socicon-youtube socicon mbr-iconfont mbr-iconfont-social text-warning"></span>
                            </a>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</section>


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

<input name="animation" type="hidden">
   <!-- <div id="scrollToTop" class="scrollToTop mbr-arrow-up"><a style="text-align: center;"><i class="mbr-arrow-up-icon mbr-arrow-up-icon-cm cm-icon cm-icon-smallarrow-up"></i></a></div> -->
  </div>
  
</template>



<script>
export default {
  head() {
    const i18nSeo = this.$nuxtI18nSeo();
    return {
      titleTemplate: `%s - La Pâtisserie Masako`,
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
          src: "/mobiris_assets/viewportchecker/jquery.viewportchecker.js"
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
          href: "/mobiris_assets/socicon/css/styles.css"
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
          href: "/mobiris_assets/animatecss/animate.min.css"
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