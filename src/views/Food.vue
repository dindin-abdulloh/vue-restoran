<template>
  <div class="food">
    <Navbar />
    <div class="container">
      <h2>Daftar <strong>Makanan</strong></h2>
     
      <div class="row col-md-8 mt-4 search-btn">
         <div class="col-md-10">
            <b-form-input
            v-model="search"
            type="text"
            placeholder="Cari makanan"
            @keyup="searchFoods"
          ></b-form-input>
         </div>
      </div>

      <div class="row mt-4">
        <div
          class="col-md-4 mt-3"
          v-for="product in products"
          :key="product.id"
        >
          <CardProduct :product="product" />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Navbar from "../components/Navbar.vue";
import CardProduct from "../components/CardProduct.vue";
import axios from "axios";
export default {
  name: "Food",
  components: {
    Navbar,
    CardProduct,
  },
  data() {
    return {
      products: [],
    };
  },

  methods: {
    setProduct(data) {
      this.products = data;
    },
    searchFoods(){
      axios
      .get("http://localhost:3000/products?q="+this.search)
      .then((response) => this.setProduct(response.data))
      .catch((error) => console.log("Gagal", error));
    }
  },

  mounted() {
    axios
      .get("http://localhost:3000/products")
      .then((response) => this.setProduct(response.data))
      .catch((error) => console.log("Gagal", error));
  },
};
</script>

<style></style>
