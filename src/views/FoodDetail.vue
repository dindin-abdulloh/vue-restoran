<template>
  <div class="food-detail">
    <Navbar />
    <div class="container">
      <!-- Breadcrumb -->
      <div class="row mt-4">
        <div class="col">
          <nav aria-label="breadcrumb">
            <ol class="breadcrumb">
              <li class="breadcrumb-item">
                <router-link to="/" class="text-dark">Home</router-link>
              </li>
              <li class="breadcrumb-item">
                <router-link to="/foods" class="text-dark">Foods</router-link>
              </li>
              <li class="breadcrumb-item active" aria-current="page">
                Food Order
              </li>
            </ol>
          </nav>
        </div>
      </div>
      <!-- /Breadcrumb -->

      <div class="row">
        <div class="col-md-6">
          <img
            :src="'../assets/images/' + product.gambar"
            alt=""
            class="img-fluid shadow"
          />
        </div>

        <div class="col-md-6">
          <b-card bg-variant="light">
            <b-form-group
              label-cols-lg="3"
              label-size="lg"
              label-class="font-weight-bold pt-0"
              class="mb-0"
            >
              <div class="col">
                <h4>{{ product.nama }}</h4>
              </div>
              <hr />
              <div class="col">
                <h5>Harga : Rp. {{ product.harga }}</h5>
              </div>

              <div class="col mt-3">
                <label for="jumlah">Jumlah Pesanan</label>
                <b-form-input id="jumlah"></b-form-input>
              </div>

              <div class="col mt-3">
                <label for="keterangan">Keterangan</label>

                <b-form-textarea
                  id="textarea-default"
                  placeholder="Keterangan"
                ></b-form-textarea>
              </div>

              <div class="col mt-4">
                <router-link to="/foods" class="btn btn-success float-right"
                  ><b-icon-chart></b-icon-chart> Pesan</router-link
                >
              </div>
            </b-form-group>
          </b-card>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Navbar from "../components/Navbar.vue";
import axios from "axios";

export default {
  name: "FoodDetail",
  components: {
    Navbar,
  },
  data() {
    return {
      product: {},
    };
  },
  methods: {
    setProduct(data) {
      this.product = data;
    },
  },
  mounted() {
    axios
      .get("http://localhost:3000/products/" + this.$route.params.id)
      .then((response) => this.setProduct(response.data))
      .catch((error) => console.log("Gagal", error));
  },
};
</script>

<style></style>
