<template>
  <div>
    <section class="cid-rThonCdHbq mbr-fullscreen" data-bg-video="https://youtu.be/di5OX6V7QlA" id="header2-1">
      <div class="mbr-overlay" style="opacity: 0.5; background-color: rgb(234, 227, 241);"></div>
      <div class="container align-center">
        <div class="row justify-content-md-center">
          <div class="mbr-white col-md-10">
            <img src="/mobiris_assets/images/logo.png" alt="">
              <!-- <h1 class="mbr-section-title mbr-bold pb-3 mbr-fonts-style display-1">h</h1> -->
              
              <!-- <p class="mbr-text pb-3 mbr-fonts-style display-5">
                  Masako手作日法甜點 - La Pâtisserie Masako<br>神戶·巴黎·台北 - 有溫度的甜點故事<br></p> -->
              
          </div>
        </div>
      </div>
      <div class="mbr-arrow hidden-sm-down" aria-hidden="true">
        <a href="#next">
          <i class="mbri-down mbr-iconfont"></i>
        </a>
      </div>
    </section>
    <section class="mbr-section article content9 cid-rThoGB6r4t" id="content9-2">
      <div class="container">
        <div class="inner-container" style="width: 100%;">
          <hr class="line" style="width: 25%;">
          <div class="section-text align-center mbr-fonts-style display-5">
            神戶 · 巴黎 · 台北 - 有溫度的甜點故事
          </div>
          <hr class="line" style="width: 25%;">
        </div>
      </div>
    </section>

    <section class="mbr-section content5 cid-rTiHS5TSrc mbr-parallax-background" id="content5-o" style="background-image:url('https://scontent.ftpe8-4.fna.fbcdn.net/v/t1.0-9/p960x960/86281899_2779882345572286_5302322592189775872_o.jpg?_nc_cat=104&_nc_sid=9e2e56&_nc_ohc=8aglvF21lV8AX9vvtdM&_nc_ht=scontent.ftpe8-4.fna&_nc_tp=6&oh=f15f89102e41a2f5956a6b32bdbd7cd1&oe=5E94DEFE')">

    

    <div class="mbr-overlay" style="opacity: 0.5; background-color: rgb(234, 227, 241);">
    </div>

    <div class="container">
        <div class="media-container-row">
            <div class="title col-12 col-md-8">
                <h2 class="align-center mbr-bold mbr-white pb-3 mbr-fonts-style display-2">
                    ARTICLE HEADER
                </h2>
                <h3 class="mbr-section-subtitle align-center mbr-light mbr-white pb-3 mbr-fonts-style display-5">
                    Article header with background image and parallax effect
                </h3>
                
                
            </div>
        </div>
    </div>
</section>

  </div>
</template>
<script>
export default {
  layout: 'mobirise',
  async asyncData({ app }) {
    const lang = app.i18n.locale === "ja" ? "ja-jp" : "zh-tw";
    const document = await app.$prismic.api.getSingle("home", { lang });
    if (document) {
      return { document };
    } else {
      error({ statusCode: 404, message: "Page not found" });
    }
  },
  head() {
    return {
      title: this.$prismic.asText(this.document.data.title),
      meta: [
        {
          hid: "description",
          name: "description",
          content: this.$prismic.asText(this.document.data.summary)
        },
        {
          vmid: "og:image",
          property: "og:image",
          content: this.document.data.og_image.url
        }
      ]
    };
  },
  methods:{
    loadJs(path){
      const script = document.createElement("script");
      script.defer = true;
      script.src = path;
      document.getElementsByTagName("head")[0].appendChild(script);
    }
  },
  mounted() {
    this.loadJs('/mobiris_assets/bootstrapcarouselswipe/bootstrap-carousel-swipe.js')
    this.loadJs('/mobiris_assets/theme/js/script.js')
    this.loadJs('/mobiris_assets/gallery/player.min.js')
    this.loadJs('/mobiris_assets/gallery/script.js')
    this.loadJs('/mobiris_assets/slidervideo/script.js')

  },
};
</script>