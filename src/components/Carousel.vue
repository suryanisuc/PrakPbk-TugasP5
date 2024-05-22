<template>
    <q-carousel
      v-model="slide"
      :autoplay="true"
      navigation
      swipeable
      animated
      infinite
    >
      <q-carousel-slide
        v-for="(img, index) in images"
        :key="index"
        :name="index"
        :img-src="img"
      />
    </q-carousel>
  </template>
  
  <script>
  export default {
    name: 'Carousel',
    props: {
      images: {
        type: Array,
        required: true
      }
    },
    data() {
      return {
        slide: 0
      }
    }
  }
  </script>
  