<template>
      <b-carousel
      id="carousel-1"
      :interval="0"
      indicators
      background="#ababab"
      img-width="1024"
      img-height="480"
      style="text-shadow: 1px 1px 2px #333 !important;"
    >
      <!-- Text slides with image -->
      <slot name="main"></slot>
      <b-carousel-slide 
        img-src="https://picsum.photos/1024/480/?image=52">
      </b-carousel-slide>
      <!-- 
      <b-carousel-slide 
        img-src="https://picsum.photos/1024/480/?image=52">
      </b-carousel-slide> -->
  </b-carousel>
</template>
<script>
export default {

}
</script>
<style scoped>
.carousel-caption {
    position: absolute !important;
    right: 0 !important;
    bottom: 0 !important;
    left: 0 !important;
    z-index: 10 !important;
    padding-top: 0 !important;
    padding-bottom: 0 !important;
    color: #fff !important;
    text-align: center !important;
    width: 100% !important;
    height: 100% !important;
}
</style>