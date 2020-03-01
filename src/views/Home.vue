<template>
  <div class="home">
    <HeaderStore />

  </div>
</template>

<script>
// @ is an alias to /src
// import HelloWorld from '@/components/HelloWorld.vue'
import HeaderStore from '@/components/HeaderStore.vue'


export default {
  name: 'Home',
  components: {
    HeaderStore
  }
}
</script>
