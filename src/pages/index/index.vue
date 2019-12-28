<template>
  <div >
    <swiper
      :indicator-dots="indicatorDots"
      :autoplay="autoplay"
      :interval="interval"
      :duration="duration"
      style="height:620px"
    >
      <block v-for="img in imgUrls" :key="img">
        <swiper-item > 
          <image :src="img"  style="width:100%;height:100%;"/>
        </swiper-item>
      </block>
    </swiper>
  </div>
</template>

<script>
export default {
  data () {
    return{
       imgUrls: [
        "http://photocdn.sohu.com/20120705/Img347309849.jpg",
        "http://spider.ws.126.net/2c576a6ab427c1e72b3cc02303807542.jpeg",
        "http://img3.cache.netease.com/game/2010/11/30/20101130104206a3013.jpg",
        "http://www.musiceol.com/news/html/2010-12/images/20101223214941973.jpg"
      ],
      indicatorDots: true,
      autoplay: true,
      interval: 4000,
      duration: 1000  
    }
  },
  

  methods: {
  },

  created () {
  }
}
</script>

<style scoped>

</style>
