<script setup>
import {ref} from 'vue'
</script>

<template>
  <nav class="navbar fixed-top navbar-dark bg-dark border-bottom border-body">
    <div class="container-fluid">
      
      <router-link class="navbar-brand" to="/"><img src="./assets/logo.png" alt="" width="200"> </router-link>
      <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav" aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="collapse navbar-collapse" id="navbarNav">
        <ul class="navbar-nav">
          <li class="nav-item">
            
            <router-link class="nav-link" aria-current="page" to="/">Início</router-link>
          </li>
          <li class="nav-item">
            
            <router-link class="nav-link" to="/about">Sobre</router-link>
          </li>
        </ul>
      </div>
    </div>
  </nav>

  <div class="main">
    <router-view></router-view>
  </div>

  <footer class=" fixed-bottom bg-dark text-light">
    <div>
      Unimar | ADS | {{ new Date().getFullYear() }}
    </div>
  </footer>
</template>
<style>
footer{
  position: fixed ;
  bottom: 0;
  width: 100%;
  display: flex;
  align-items: center;
  justify-content: center;
  height: 40px;
}
</style>