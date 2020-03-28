<template>
  <div>
    <section class="header7 cid-rTiQvm7Dhm mbr-parallax-background" id="header7-17"  :style="{ backgroundImage: `url('${document.data.og_image.url}')` }">
      <div class="mbr-overlay" style="opacity: 0.6; background-color: rgb(51, 51, 51);">
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
            <!-- <div class="mbr-section-btn">
              <a
                v-if="document.data.status === 'selling'"
                :href="document.data.buylink.url"
                class="btn btn-md btn-primary display-4"
              >前往購買</a>
              <a
                v-else-if="document.data.status === 'out_of_stock'"
                disabled
                class="btn btn-md btn-primary display-4"
              >缺貨中</a>
              <a
                v-else-if="document.data.status === 'not_season'"
                disabled
                class="btn btn-md btn-primary display-4"
              >目前非產季</a>
            </div> -->
          </div>
          <div v-if="$prismic.asText(document.data.youtube_video_id)" class="mbr-figure" style="width: 100%;">
            <iframe 
              class="mbr-embedded-video" 
              width="1280" 
              height="720" 
              :src="`https://www.youtube.com/embed/${$prismic.asText(document.data.youtube_video_id)}?controls=0&autoplay=1&mute=1&loop=1&showinfo=0&playlist=${$prismic.asText(document.data.youtube_video_id)}`" 
              frameborder="0" 
              allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" 
              allowfullscreen></iframe>
          </div>
        </div>
      </div>
    </section>

    <section class="features11 cid-rTiQaASfXR" id="features11-16">
      <div class="container">   
        <div class="col-md-12">
          <div class="media-container-row">
            <div class="mbr-figure m-auto" style="width: 50%;">
              <img
                :alt="document.data.main_image.alt"
                :src="document.data.main_image.url"
              />
            </div>
            <div class=" align-left aside-content">
              <h2 class="mbr-title pt-2 mbr-fonts-style display-2">
                {{$prismic.asText(document.data.title)}}
              </h2>
              <div class="mbr-section-text">
                <p class="mbr-text mb-5 pt-3 mbr-light mbr-fonts-style display-7" v-html="$prismic.asHtml(document.data.description)">
                </p>
                <h4 class="mbr-title mbr-fonts-style display-5">
                  {{$prismic.asText(document.data.price_desc)}}
                </h4>
              </div>
              <div class="block-content">
                <div class="card p-3 pr-3">      
                  <div class="card-box">
                    <div class="mbr-section-btn">
                      <a
                        v-if="document.data.status === 'selling'"
                        :href="document.data.buylink.url"
                        class="btn btn-md btn-primary display-4"
                      >前往購買</a>
                      <a
                        v-else-if="document.data.status === 'out_of_stock'"
                        disabled
                        class="btn btn-md btn-primary display-4"
                      >缺貨中</a>
                      <a
                        v-else-if="document.data.status === 'not_season'"
                        disabled
                        class="btn btn-md btn-primary display-4"
                      >目前非產季</a>
                    </div>
                  </div>
                </div>
              </div>
            </div>
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