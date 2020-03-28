<template>
  <div>
    <section class="cid-rThonCdHbq mbr-fullscreen" data-bg-video="https://youtu.be/di5OX6V7QlA" id="header2-1">
      <div class="mbr-overlay" style="opacity: 0.6; background-color: #AD92B2;"></div>
      <div class="container align-center">
        <div class="row justify-content-md-center">
          <div class="mbr-white col-md-10">
            <img src="/mobiris_assets/images/logo.png" alt="">
              
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
          <div class="row pt-4 justify-content-center">
            <img src="/mobiris_assets/images/masako-logo.jpg" style="width:400px;">
          </div>
          <div class="section-text align-center mbr-fonts-style display-5">
            {{$prismic.asText(document.data.home_slogan)}}
          </div>
          <hr class="line" style="width: 25%;">
        </div>
      </div>
    </section>

    <section class="mbr-section content5 cid-rTiHS5TSrc mbr-parallax-background" id="content5-o" :style="{ backgroundImage: `url('${document.data.home_parallax_1_image.url}')` }">
      <div class="mbr-overlay" style="opacity: 0.6; background-color: #513B58;">
      </div>
      <div class="container">
        <div class="media-container-row">
          <div class="title col-12 col-md-8">
            <h2 class="align-center mbr-bold mbr-white pb-3 mbr-fonts-style display-2">
              {{$prismic.asText(document.data.home_parallax_1_title)}}
            </h2>
            <h3 class="mbr-section-subtitle align-center mbr-light mbr-white pb-3 mbr-fonts-style display-5">
              {{$prismic.asText(document.data.home_parallax_1_description)}}
            </h3>
          </div>
        </div>
      </div>
    </section>

    <section class="services6 cid-rThtKG45cv" id="services6-8">
      <div class="container">
        <div class="row">
          <div class="title col-12">
            <div class="section-text align-left mbr-fonts-style m-0 display-2">
              {{$prismic.asText(document.data.body[0].primary.name_of_the_gallery)}}
            </div>
          </div>
          <div v-for="(item, i) in document.data.body[0].items" :key="i" class="card col-12 pb-5">
            <nuxt-link
              :to="localePath({ name: 'products-uid', params: { uid: item.productid.uid } }, $i18n.locale)"
              class="project-description"
            >
              <div class="card-wrapper media-container-row media-container-row">
                <div class="card-box">
                  <div class="row">
                    <div class="col-12 col-md-2">
                      <div class="mbr-figure">
                        <img :src="item.gallery_image.url" :alt="item.gallery_image.alt">
                      </div>
                    </div>
                    <div class="col-12 col-md-10">
                      <div class="wrapper">
                        <div class="top-line pb-3">
                          <h4 class="card-title mbr-fonts-style display-5">
                            {{$prismic.asText(item.image_captions)}}
                          </h4>
                          <p class="mbr-text cost mbr-fonts-style m-0 display-5">
                            ${{item.image_pricetag}}
                          </p>
                        </div>
                        <div class="bottom-line">
                          <p class="mbr-text mbr-fonts-style display-7">
                            {{$prismic.asText(item.image_summary)}}
                          </p>
                        </div>
                      </div>
                    </div>
                  </div>
                </div>
              </div>
            </nuxt-link>
          </div>
        </div>
      </div>
    </section>

    <section class="testimonials3 cid-rTht2JnPyM" id="testimonials3-7">
      <div class="container">
        <div class="media-container-row">
          <div class="media-content px-3 align-self-center mbr-white py-2">
            <p 
              class="mbr-text testimonial-text mbr-fonts-style display-7" 
              v-html="$prismic.asHtml(document.data.home_about_text)">
            </p>
            <p class="mbr-author-name pt-4 mb-2 mbr-fonts-style display-7">
              林 政子 · Hayashi Masako
            </p>
            <p class="mbr-author-desc mbr-fonts-style display-7" 
              v-html="$prismic.asHtml(document.data.home_about_profo)">
            </p>
          </div>
          <div class="mbr-figure pl-lg-5" style="width: 130%;">
            <img :src="document.data.home_about_image.url" :alt="document.data.home_about_image.alt">
          </div>
        </div>
      </div>
    </section>

    <section class="mbr-section info1 cid-rTiKjFvQ0B" id="info1-r">
      <div class="container">
        <div class="row justify-content-center content-row">
          <div class="media-container-column title col-12 col-lg-7 col-md-6">
            <h3 class="mbr-section-subtitle align-left mbr-light pb-3 mbr-fonts-style display-5">
              {{$t('follow_ig')}}
            </h3>
            <iframe src="//lightwidget.com/widgets/e4da85cc06f05e42ae25985ddd925807.html" scrolling="no" allowtransparency="true" class="lightwidget-widget" style="width:100%;border:0;overflow:hidden;"></iframe>
          </div>
          <div class="media-container-column col-12 col-lg-3 col-md-4">

            <div class="mbr-section-btn align-right py-4">
              <a class="btn btn-primary display-4" target="_blank" href="https://www.instagram.com/patissiermasako">
                <span class="socicon-instagram socicon mbr-iconfont mbr-iconfont-social"></span> Follow
              </a>
            </div>

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
    this.loadJs('//cdn.lightwidget.com/widgets/lightwidget.js')   
  },
};
</script>