<template>
  
    <b-container>
      <b-card img-src="../assets/logoPokemon.png" img-alt="Card image" img-top>
        <b-card-text>
          <h4>Name : {{name}}</h4>
          Description : {{description}}
        </b-card-text>
        <b-button variant="link" href="/detailsPokemon">Link</b-button>
      </b-card>
    </b-container>
      

</template>




<script>
export default {
  name:"PokemonCard",
  props: ["name", "description"]
  
}
</script>





<style scoped>

</style>
