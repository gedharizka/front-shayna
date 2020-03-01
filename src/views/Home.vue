<template>
  <div class="home">
    <HeaderStore />
    <HeroCarousel />
    <WomanBanner />
    <HomeInsta />

  </div>
</template>

<script>
// @ is an alias to /src
// import HelloWorld from '@/components/HelloWorld.vue'
import HeaderStore from '@/components/HeaderStore.vue'
import HeroCarousel from '@/components/HeroCarousel.vue'
import WomanBanner from '@/components/WomanBanner.vue'
import HomeInsta from '@/components/HomeInsta.vue'


export default {
  name: 'Home',
  components: {
    HeaderStore,
    HeroCarousel,
    WomanBanner,
    HomeInsta
  }
}
</script>
