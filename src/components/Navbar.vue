<template>
    <div class="container">
      <nav class="navbar navbar-expand-lg navbar-light ">
  <a class="navbar-brand" href="#">Navbar</a>
  <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarNav" aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
    <span class="navbar-toggler-icon"></span>
  </button>
  <div class="collapse navbar-collapse" id="navbarNav">

    <ul class="navbar-nav"> 
        <li class="nav-item">
            <router-link class="nav-link" to="/">Home</router-link>
        </li>

        <li class="nav-item">
        <router-link class="nav-link" to="/foods">Foods</router-link>
        </li>
    </ul>

    <ul class="navbar-nav ml-auto"> 
        <li class="nav-item">
            <router-link class="nav-link" to="/keranjang">Keranjang  <b-icon icon="bag"></b-icon>
            <span class="badge badge-success ml-2">0</span>
            </router-link>
        </li>
      
        
    </ul>
  </div>
</nav>
    </div>
</template>

<script>
export default {
    name: "Navbar"
}
</script>

<style>

</style>