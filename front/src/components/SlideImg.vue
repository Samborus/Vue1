<template>
<div>
    <img :src="pics[index]" class="slider-left" />
    <img :src="pics[getNextIndex(pics, index)]" class="slider-right" />
</div>
</template>
<script>
export default {
    props: {
        pics: [],
        index: null
    },
    methods: {
        getNextIndex(pics, index) {
            if (index === pics.length - 1) {
                return 0;
            } else {
                return index + 1;
            }
        }
    }
}
</script>
<style scoped>
.slider-left , .slider-right {
    position: absolute;
    background-size: cover;
    background-position: center;   
    top: 0;
} 
.slider-left {
    left: 0;
    width: 100%;
    height: 100%;
    padding: 0;
    /* -webkit-clip-path: polygon(0 0, 90% 0, 80% 100%, 0% 100%);
    clip-path: polygon(0 0, 90% 0, 80% 100%, 0% 100%); */
}

.slider-right {
    left: 80%;
    width: 100%;
    height: 100%;
    padding: 0;
    -webkit-clip-path: polygon(10% 0, 100% 0, 100% 100%, 0% 100%);
    clip-path: polygon(10% 0, 100% 0, 100% 100%, 0% 100%);
} 

</style>