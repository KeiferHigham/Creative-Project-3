<template>
<div class="Moves">

<div class="MovieButtons">
<h2> Hello </h2>
<button @click="earlyMovies()"> early 1900s</button>
<button @click="fourties()"> 1940s</button>
<button @click="fifties()"> 1950s</button>
<button @click="sixties()"> 1960s</button>
<button @click="seventies()"> 1970s</button>
<button @click="eighties()"> 1980s</button>
<button @click="nineties()"> 1990s</button>
<button @click="twothousands()"> 2000s</button>
<button @click="twothousandtens()"> 2010+</button>

<div id="oldMovies">
<div class="movies" v-for="movie in filteredMovies" :key="movie.id">
<div class="movie">
<h2>{{movie.fullTitle}}</h2>
<img :src="movie.image">
<button @click="addFavorites(movie)"> Add To Favorites </button>
</div>
</div>


</div>



</div>
</div>


</template>


<script>

export default {
 name: 'Find',
 data: function() {
 return {
 filteredMovies: []
 }
 },
  methods: {
    earlyMovies () {
      let movie = this.$root.$data.Movies
    //  console.log(movie)
      this.filteredMovies = []

      for(let i = 0; i < movie.length; ++i) {
      if(movie[i].year < 1940) {
      this.filteredMovies.push(movie[i])
      }

      }
    },
    fourties () {
      let movie = this.$root.$data.Movies
    //  console.log(movie)
      this.filteredMovies = []

      for(let i = 0; i < movie.length; ++i) {
      if(movie[i].year >= 1940 && movie[i].year < 1950) {
      this.filteredMovies.push(movie[i])
      }

      }
    },
    fifties () {
      let movie = this.$root.$data.Movies
    //  console.log(movie)
      this.filteredMovies = []

      for(let i = 0; i < movie.length; ++i) {
      if(movie[i].year >= 1950 && movie[i].year < 1960) {
      this.filteredMovies.push(movie[i])
      }

      }

    },
    sixties () {
      let movie = this.$root.$data.Movies
    //  console.log(movie)
      this.filteredMovies = []

      for(let i = 0; i < movie.length; ++i) {
      if(movie[i].year >= 1960 && movie[i].year < 1970) {
      this.filteredMovies.push(movie[i])
      }

      }

    },
    seventies () {
      let movie = this.$root.$data.Movies
    //  console.log(movie)
      this.filteredMovies = []

      for(let i = 0; i < movie.length; ++i) {
      if(movie[i].year >= 1970 && movie[i].year < 1980) {
      this.filteredMovies.push(movie[i])
      }

      }

    },
    eighties () {
      let movie = this.$root.$data.Movies
    //  console.log(movie)
      this.filteredMovies = []

      for(let i = 0; i < movie.length; ++i) {
      if(movie[i].year >= 1980 && movie[i].year < 1990) {
      this.filteredMovies.push(movie[i])
      }

      }

    },
    nineties () {
      let movie = this.$root.$data.Movies
    //  console.log(movie)
      this.filteredMovies = []

      for(let i = 0; i < movie.length; ++i) {
      if(movie[i].year >= 1990 && movie[i].year < 2000) {
      this.filteredMovies.push(movie[i])
      }

      }

    },
    twothousands () {
      let movie = this.$root.$data.Movies
    //  console.log(movie)
      this.filteredMovies = []

      for(let i = 0; i < movie.length; ++i) {
      if(movie[i].year >= 2000 && movie[i].year < 2010) {
      this.filteredMovies.push(movie[i])
      }

      }

    },
    twothousandtens () {
      let movie = this.$root.$data.Movies
    //  console.log(movie)
      this.filteredMovies = []

      for(let i = 0; i < movie.length; ++i) {
      if(movie[i].year >= 2010) {
      this.filteredMovies.push(movie[i])
      }

      }

    },
    addFavorites (movie) {
     console.log("helloooo")
     this.$root.$data.Favorites.push(movie);


     return ""
    }


  },


}


</script>
