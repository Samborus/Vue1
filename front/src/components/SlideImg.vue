<template>
<div>
    <img :src="pics[index]" class="slider-left" />
    <!-- <img :src="pics[index + 1]" class="slider-right" /> -->
</div>
</template>
<script>
export default {
    props: {
        pics: [],
        index: null
    },
}
</script>
<style scoped>
.slider-left , .slider-right {
  position: absolute;
  background-size: cover;
  background-position: center;   
} 
.slider-left {
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    padding: 0;
    -webkit-clip-path: polygon(0 0, 90% 0, 80% 100%, 0% 100%);
    clip-path: polygon(0 0, 90% 0, 80% 100%, 0% 100%);
}

.slider-right {
    left: 90%;
    width: 100%;
    height: 100%;
    padding: 0;
    /* -webkit-clip-path: polygon(0 0, 90% 0, 80% 100%, 0% 100%);
    clip-path: polygon(0 0, 90% 0, 80% 100%, 0% 100%); */
} 

</style>