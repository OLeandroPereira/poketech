<script setup>
  const pokemon = defineProps(["img", "name", "hp", "loading"])

</script>

<template>
  <div class="card CardPokemonSelected"
  :class="loading ? '' : 'animate__animated animate__flipInX'"
  >
    <img 
    v-if="pokemon.name"
    :src="pokemon.img"
    height="250" 
    class="card-img-top pt-2" 
    :alt="pokemon.name"
    >

    <img 
    v-else
    src="../assets/egg_pokemon.svg"
    :src="pokemon.img"
    height="250" 
    class="card-img-top pt-2" 
    :alt="pokemon.name"
    >

    <div class="card-body text-center">
      <h5 class="card-title text-center">{{ pokemon.name || '???'}}</h5>
      <hr>
      
        <div class="row">
          <div class="col d-inline-block p-100" style='text-align:left'>
            <h5>Base de stats:</h5>
            <div>
              <strong>HP:</strong>
              <span>{{ pokemon.hp }}</span>
            </div>
            <div>
              <strong>ATTACK:</strong>
              <span>50</span>
            </div>    
            <div>
              <strong>DEFENSE:</strong>
              <span>50</span>
            </div>
            <div>
              <strong>SPECIAL ATTACK:</strong>
              <span>50</span>
            </div>
            <div>
              <strong>SPECIAL DEFENSE:</strong>
              <span>50</span>
            </div>    
            <div> 
              <strong>SPEED:</strong>
              <span>50</span>
            </div>
          </div>
          
          <div class="col perfil">
            <img src="../assets/Foto.png" class="card-img-top" alt="Desenvolvedor do App">
          </div> 
          <div class="col m-auto">
            <strong>Desenvolvedor<br>Front-end</strong>
            <hr>
            <p>Leandro Pereira</p>
          </div> 
      </div>
    </div>
  </div>
</template>

<style scoped>
  .perfil img{
    max-width: 100%;
    border-radius: 50%;
    border: 9px solid #eebe65;
  }

  .CardPokemonSelected {
    max-height: 70vh;
    color: #fff;
    background: rgb(2,0,36);
    background: linear-gradient(90deg, rgba(2,0,36,1) 0%, rgba(9,96,121,1) 35%, rgba(0,212,255,1) 100%);
  }

</style>