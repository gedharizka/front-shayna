<template>
  <!-- Women Banner Section Begin -->
  <section class="women-banner spad">
    <div class="container-fluid">
      <div class="row">
        <div class="col-lg-12 mt-5" v-if="products.length > 0">
          <carousel class="product-slider" :dots="false" :items="3" :nav="false" :autoplay="true">

            <div class="product-item" v-for="itemProducts in products" v-bind:key="itemProducts.id">
              <div class="pi-pic">
                <img v-bind:src="itemProducts.galleries[0].photo" alt />
                <ul>
                  <li class="w-icon active">
                    <a href="#">
                      <i class="icon_bag_alt"></i>
                    </a>
                  </li>
                  <li class="quick-view">
                    <router-link v-bind:to="'/product/'+itemProducts.id">+ Quick View</router-link>
                  </li>
                </ul>
              </div>
              <div class="pi-text">
                <div class="catagory-name">{{itemProducts.type}}</div>
                <router-link to="/product">
                  <h5>{{itemProducts.name}}</h5>
                </router-link>
                <div class="product-price">
                  ${{itemProducts.price}}
                  <span>$35.00</span>
                </div>
              </div>
            </div>

          </carousel>
          <!-- Carousel -->
        </div>
        <div class="col-lg-12" v-else>
          <p>
            Produk terbaru belum tersedia untuk saat ini
          </p>
        </div>
      </div>
    </div>
  </section>
  <!-- Women Banner Section End -->
</template>


<script>
import carousel from 'vue-owl-carousel'
import axios from 'axios'

export default {
  name:"WomanBanner",
  components:{
    carousel
  },
  data(){
    return {
      products:[]
    }
  },
  mounted(){
    axios
      .get("http://127.0.0.1:8000/api/products")
      // .get("http://shayna-backend.belajarkoding.com/api/products")
      .then(res=> (this.products = res.data.data.data))
      .catch(err => console.log(err))
  }
};
</script>

<style scoped>
  .product-item{
    margin-right: 25px
  }
  /* .pi-pic{
    height: 340px;
  } */
</style>