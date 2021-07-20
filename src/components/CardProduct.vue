<template>
  <div>
    <b-card
      :title= 'product.nama'
      :img-src= "'assets/images/'+ product.gambar"
      img-alt="Image"
      img-top
      tag="article"
      style="max-width: 20rem;"
      class="mb-4 shadow card-product"
    >
      <b-card-text>
       Harga: Rp. {{ product.harga }}
      </b-card-text>

      <router-link :to="'/foods/'+ product.id" class="btn btn-success"><b-icon-cart></b-icon-cart> Pesan</router-link>
    </b-card>
  </div>
</template>

<script>
export default {
  name: "CardProduct",
  props: ["product"],
};
</script>

<style></style>
