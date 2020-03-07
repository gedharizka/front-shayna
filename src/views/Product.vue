<template>
  <div class="product">
    <HeaderStore />
    <p>ini halaman product</p>
    <Footer />

  </div>
</template>

<script>
// @ is an alias to /src
// import HelloWorld from '@/components/HelloWorld.vue'
import HeaderStore from '@/components/HeaderStore.vue'
import Footer from '@/components/Footer.vue'




export default {
  name: 'Product',
  components: {
    HeaderStore,
    Footer
  }
}
</script>
