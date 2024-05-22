<template>
  <q-layout view="lHh Lpr lFf">
    <navbar :title="storeTitle" @toggle-left-drawer="toggleLeftDrawer"/>
    <left-drawer :model-value="leftDrawerOpen" @update:model-value="updateLeftDrawer"/>

    <q-page-container>
      <carousel :images="carouselImages" />

      <q-page padding>
        <div class="row q-col-gutter-md">
          <div class="col-xs-12 col-sm-6 col-md-4" v-for="product in products" :key="product.id">
            <card 
              :title="product.title" 
              :description="product.description" 
              :image="product.image" 
              @view-details="viewDetails(product.id)"
            />
          </div>
        </div>
      </q-page>
    </q-page-container>

    <Footer />
  </q-layout>
</template>

<script>
import Navbar from './components/Navbar.vue'
import Carousel from './components/Carousel.vue'
import Card from './components/Card.vue'
import Footer from './components/Footer.vue'
import LeftDrawer from './components/LeftDrawer.vue'

export default {
  name: 'App',
  components: {
    Navbar,
    Carousel,
    Card,
    Footer,
    LeftDrawer
  },
  data() {
    return {
      storeTitle: 'Suci Store',
      leftDrawerOpen: true,
      carouselImages: [
        'https://images.pexels.com/photos/205961/pexels-photo-205961.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=1',
        'https://images.pexels.com/photos/375904/pexels-photo-375904.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=1',
        'https://images.pexels.com/photos/4946614/pexels-photo-4946614.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=1'
      ],
      products: [
        { id: 1, title: 'Salad Cake', description: 'Rp 35.000.00', image: 'https://images.pexels.com/photos/1099680/pexels-photo-1099680.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=1' },
        { id: 2, title: 'Ramen Kari', description: 'Rp 48.500.00', image: 'https://images.pexels.com/photos/699953/pexels-photo-699953.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=1' },
        { id: 3, title: 'Pizza Sosis', description: 'Rp 55.000.00', image: 'https://images.pexels.com/photos/825661/pexels-photo-825661.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=1' }
      ],
      
    }
  },
  methods: {
    toggleLeftDrawer() {
      this.leftDrawerOpen = !this.leftDrawerOpen;
    },
    updateLeftDrawer(val) {
      this.leftDrawerOpen = val;
    },
    viewDetails(productId) {
      console.log('View details for product:', productId);
    }
  }
}
</script>
