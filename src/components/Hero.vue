<template>
  <div class="hero">
    <!-- Dekstop -->
    <div class="d-none d-md-block">
      <div class="row mt-4">
        <div class="col-md-6 justify-content-center align-self-center">
          <h2><strong>Delicius foods,</strong></h2>
          <h5>In Your Gadget</h5>
          <p>Ayo pilih dan pesan makanan favorit Anda</p>
          <router-link to="/foods" class="btn btn-success"
            ><b-icon-arrow-right></b-icon-arrow-right> Pesan</router-link
          >
        </div>
        <div class="col-md-6">
          <!-- #6BFF63 -->
          <img src="../assets/images/hero.png" width="100%" />
        </div>
      </div>
    </div>

    <!-- Mobile -->
    <div class="d-sm-block d-md-none">
      <div class="row mt-4">
        <div class="col-md-6 mb-4">
          <!-- #6BFF63 -->
          <img src="../assets/images/hero.png" width="100%" />
        </div>
        <div class="col-md-6 justify-content-center align-self-center">
          <h2><strong>Delicius foods,</strong></h2>
          <h5>In Your Gadget</h5>
          <p>Ayo pilih dan pesan makanan favorit Anda</p>
          <!-- <router-link class="mt-3 nav-link" variant="success" to="/foods"><b-icon-arrow-right /> Pesan</router-link> -->
          <router-link to="/foods" class="btn btn-success"
            ><b-icon-arrow-right></b-icon-arrow-right> Pesan</router-link
          >
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Hero",
};
</script>

<style></style>
