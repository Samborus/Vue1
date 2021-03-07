<template>
  <div class="home">
    <carousel>
      <template v-slot:main>
          <b-carousel-slide v-for="(pic, i) in pics" :key="i" img-blank img-alt="no image">
           <slide-img :index="i" :pics="pics">
           </slide-img>
          </b-carousel-slide>
      </template>
    </carousel>
  </div>
</template>

<script>
import Carousel from '../components/Carousel.vue'
import SlideImg from '../components/SlideImg.vue';

export default {
  name: 'Home',
   data() {
        return {
          pics: []
        }
   },
   mounted() {
     this.pics = ['https://picsum.photos/1024/480/?image=50', 'https://picsum.photos/1024/480/?image=51', 'https://picsum.photos/1024/480/?image=52'];
     console.log(this.pics);
   },
  components: {
    Carousel,
    SlideImg    
  }
}
</script>
<style scoped>
.home {
  position: relative;
  display: block;
  opacity: 1;
}
</style>
