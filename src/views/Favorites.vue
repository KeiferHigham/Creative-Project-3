<template>
  <div>
    <h1>My Favorties list</h1>
    <div id="favorites">
      <div class="movies" v-for="(movie, index) in Favorites" :key="movie.id">
        <div class="movie">
        <input type="text" placeholder ="Edit Title" v-model="newTitle"/>
    <button @click="Edit(index)">Edit Title</button>
          <h2>{{movie.fullTitle}}</h2>
          <div class="movieGroup">
          <img :src="movie.image">
          <button @click="Remove(index)"> Remove </button>
        </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>

export default {
 name: 'Favorites',
 data: function() {
   return {
     Favorites: this.$root.$data.Favorites,
     newTitle: ""
   }
 },
  methods: {
    Remove (movieIndex) {
      this.$root.$data.Favorites.splice(movieIndex, 1);
    },
    Edit (movieIndex) {
    this.$root.$data.Favorites[movieIndex].fullTitle = this.newTitle;
    this.newTitle = ""
    }
  }
}
</script>

<style scoped>
  .movieGroup {
    display: flex;
    flex-direction: column;
  }

  #favorites {
    margin-bottom: 55px;
    display: flex;
    flex-direction: row;
    flex-wrap: wrap;
    justify-content: space-around;
  }

  .movie {
    width: 300px;
  }

</style>
