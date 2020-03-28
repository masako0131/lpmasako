<template>
  <div>

    
    <section class="header7 cid-rTiQvm7Dhm mbr-parallax-background" id="header7-17"  :style="{ backgroundImage: `url('${document.data.og_image.url}')` }">
      <div class="mbr-overlay" style="opacity: 0.6; background-color: #4F4F4F;">
      </div>
      <div class="container">
          <div class="media-container-row">

              <div class="media-content align-right">
                  <h1 class="mbr-section-title mbr-white pb-3 mbr-fonts-style display-1">
                      {{$prismic.asText(document.data.title)}}
                  </h1>
                  <div class="mbr-section-text mbr-white pb-3">
                      <p 
                        class="mbr-text mbr-fonts-style display-5"
                        v-html="$prismic.asHtml(document.data.summary)">
                      </p>
                  </div>
                  <div class="mbr-section-btn">
                          <a class="btn btn-md btn-primary display-4" href="https://mobirise.co">LEARN MORE</a>
                          <a class="btn btn-md btn-white-outline display-4" href="https://mobirise.co">LIVE DEMO</a>
                  </div>
              </div>

              <div class="mbr-figure" style="width: 100%;">
                <iframe 
                  class="mbr-embedded-video" 
                  width="1280" 
                  height="720" 
                  src="https://www.youtube.com/embed/zA3JhPlDKog?controls=0&autoplay=1&mute=1&loop=1&showinfo=0&playlist=zA3JhPlDKog" 
                  frameborder="0" 
                  allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" 
                  allowfullscreen></iframe>
              </div>


          </div>
      </div>
  </section>

    
  </div>
</template>

<script>
function getPage(prismic, uid, lang) {
  return prismic.api.getByUID("product", uid, {
    lang
  });
}

export default {
  layout: 'mobirise',
  async asyncData({ app, params }) {
    const lang = app.i18n.locale === "ja" ? "ja-jp" : "zh-tw";
    const document = await getPage(app.$prismic, params.uid, lang);
    if (document) {
      return { document };
    } else {
      //error({ statusCode: 404, message: "Page not found" });
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
  components: {},
  methods:{
    loadJs(path){
      const script = document.createElement("script");
      script.defer = true;
      script.src = path;
      document.getElementsByTagName("head")[0].appendChild(script);
    }
  },
  async created() {
  },
  async mounted() {
    this.loadJs('/mobiris_assets/theme/js/script.js')
  }
};
</script>