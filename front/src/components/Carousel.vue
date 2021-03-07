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
      <slot name="main"></slot>
  </b-carousel>
</template>
<script>
export default {

}
</script>
<style scoped>
</style>