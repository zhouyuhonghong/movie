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
        'https://images.unsplash.com/photo-1551334787-21e6bd3ab135?w=640',
        'https://images.unsplash.com/photo-1551214012-84f95e060dee?w=640',
        'https://images.unsplash.com/photo-1551446591-142875a901a1?w=640'
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
