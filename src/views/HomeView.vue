<script setup>
import {onMounted, reactive, ref} from 'vue';
import ListPersonagens from '../components/ListPersonagem.vue';

let personagens = reactive(ref())

onMounted(() => {
  fetch("https://rickandmortyapi.com/api/character")
  .then(response => response.json())
  .then(response =>{
    personagens.value = response.results
  });
})

</script>

<template>
  <main>
    <div class="container-fluid mt-5">
      <div class="col-lg-12">
        <div class="card-body row">
          <ListPersonagens
          v-for="personagem in personagens"
          :key="personagem.id"
          :name="personagem.name"
          :url="personagem.url"
          :image="personagem.image"
          :status="personagem.status"
          :gender="personagem.gender"
          :species="personagem.species"
          :location="personagem.location.name"
          :episodes= "personagem.episode"
          />
        </div>
      </div>
    </div>
  </main>
</template>



