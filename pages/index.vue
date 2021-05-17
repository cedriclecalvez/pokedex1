<template>
    <div>  
        <h1 class="display-3">Pokédex</h1> 
        <div class="card-deck ">              
            <PokemonCard v-for="pokemon in pokemons" v-bind:name="pokemon.name" v-bind:description="pokemon.description"/>
        </div> 
    </div>
</template>




<script>
    import PokemonCard from '@/components/PokemonCard.vue'


// const pokemonIds = [1,2,3,4]

// const pokemons = pokemonIds.map(id => 
//     fetch(`https://pokeapi.co/api/v2/pokemon/${id}`)
//     .then(res => res.json())
//         .then(json => {
//           console.log("JSON",json.name)
//           return json
//     })
// )

   
        let pokemons = []

        const allPokemons=[]
             var requestOptions = {
             method: 'GET',
             redirect: 'follow'
             };

         fetch("https://pokeapi.co/api/v2/pokemon/?limit=151", requestOptions)
        .then(response => response.text())
        .then (result => {console.log("RESULT",result); pokemons= allPokemons.push(result.results) })
        .catch(error => console.log("ERROR", error));
          
        
       
        console.log("pokemons",pokemons)
        


     
    export default {



        components:{
            PokemonCard
               
            },


            data(){
                console.log(this)
                this.$fetch
                // console.log("pokeName0",this.posts[0].name)


                return{
                    
                    pokemons:[
                        {name:pokemons[0], description:"33 eqhrhreheqrhqehetqhqehhqhQHQththQ"},
                        {name:'bulbizar2', description:"33 eqhrhreheqrhqehetqhqehhqhQHQththQ"},
                        {name:'bulbizar3', description:"33 eqhrhreheqrhqehetqhqehhqhQHQththQ"},
                        {name:'bulbizar4', description:"33 eqhrhreheqrhqehetqhqehhqhQHQththQ"},
                        {name:'bulbizar5', description:"33 eqhrhreheqrhqehetqhqehhqhQHQththQ"},
                        {name:'bulbizar6', description:"33 eqhrhreheqrhqehetqhqehhqhQHQththQ"},
                        {name:'bulbizar7', description:"33 eqhrhreheqrhqehetqhqehhqhQHQththQ"},
                        {name:'bulbizar8', description:"33 eqhrhreheqrhqehetqhqehhqhQHQththQ"},
                        {name:'bulbizar9', description:"33 eqhrhreheqrhqehetqhqehhqhQHQththQ"},
                    ],
                     posts:[]
                }
                 
            },
            
            // async fetch() {
            //     this.posts = await fetch('https://pokeapi.co/api/v2/pokemon/?limit=151')
            //     .then(res => res.json())
            //     .then(json => {console.log("JSON name:",json.results[0].name)
            //     console.log("json JSON RESULTS : ",json.results)

            //     const pokeName0 = json.results[0].name
            //     console.log("pokeName0 : ",pokeName0)

            //     for (let i=0; i<json.results[i].name.length; i++){
            //         const names = allName.push(results[i].name)
            //         console.log("NAMES",names)
            //     }     

                
            //     this.resultspoke = json.results
            //     return (pokeName0,json.results)
                
            //     })
            // }

        }


</script>




<style scoped>
  
    .image{
      justify-content: center;
      align-content: center;
      width: 50vw;
    }
    
</style>


