<template>
  <div id="app">
  <entre v-on:formsub="api"></entre>
  <sortie v-bind:affiche="affiche"></sortie>
    </div>
</template>

<script>
import entre from './components/entre'
import sortie from './components/sortie'



export default {
  name: 'app',
  components: {
    entre,
    sortie
  },
  data(){
    return {
      affiche:''
    }
  },
  methods: {
    api(titre){
      this.$http.get('https://netflixroulette.net/api/api.php?title='+ titre)
      .then((response) => {
        this.affiche=response.body
        console.log(response.body);
  });
    }
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

body {
  background-color: black;
  color: white;
}


</style>
