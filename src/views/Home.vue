<template>
  <div class="home">
    <h1>Movies</h1>
    <p>Welcome to the favorite movies list creator. Click <strong>Find</strong> above to search for your favorites!!</p>


    <div class="movies">
    <div v-for="movie in filteredMovies" :key="movie.id">
      <div class="movieImg">
        <img :src="movie.image">
      </div>
    </div>
  </div>
</div>
</template>

<script>
// @ is an alias to /src

export default {
  name: 'Home',
  data() {
    return {
      filteredMovies: []
    }
  },
  created() {
    this.earlyMovies()
  },
  components: {

  },
  methods: {
    earlyMovies () {
      let movie = this.$root.$data.Movies
      //console.log(movie)
      this.filteredMovies = []

      for(let i = 0; i < movie.length; i += 25) {
        this.filteredMovies.push(movie[i])

      }


    },
  }
}
</script>


<style scoped>
  .home h1 {
    font-style: italic;
    color: black;
    font-size: 100px;
  }

  p {
    font-size: 50px;
  }
  .movies {
    display: flex;
    flex-direction: row;
    flex-wrap: wrap;
    justify-content: space-around;
    /*border: 5px solid red;*/
    margin-bottom: 55px;
  }
  .movieImg {

  }
</style>
