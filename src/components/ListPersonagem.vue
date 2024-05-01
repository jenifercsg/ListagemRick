<script setup>
    const personagem = defineProps(["name", "url", "image", "status", "gender", "species", "location", "episodes"])
    import {ref} from "vue";

</script>


<template>
      <div class="card col-lg-12 mt-5" style="width: 18rem; height: 790px">
        <img :src="personagem.image" class="img-fluid rounded-start mt-5" alt="Imagem de {{ personagem.name }}">
        <div class="card-body">
          <h5 class="card-title"> {{ personagem.name }}</h5>
        </div>
        <ul class="list-group list-group-flush"  style="font-size: 150%; font-family: serif;" >
          <li class="list-group-item">STATUS: {{ personagem.status}}</li>
          <li class="list-group-item">ESPÉCIE: {{personagem.species}}</li>
          <li class="list-group-item">GÊNERO: {{personagem.gender}}</li>
          <li class="list-group-item">LOCALIZAÇÃO ATUAL: {{ personagem.location}}</li>
          <li class="list-group-item">EPISÓDIOS: {{ personagem.episodes.length}} </li>
        </ul>
      </div>
</template>

