<template>
  <div id="app">
    <div id="nav">
      <router-link to="/">Home</router-link> |
      <router-link to="/Favorites">Favorites</router-link> |
      <router-link to="/Find">Find</router-link>
    </div>
    <router-view/>
  <p> {{GetFirstItem}} </p>
  <div class="github-footer-fixed"><a href='https://github.com/KeiferHigham/Creative-Project-3.git'>Github Repository</a></div>
  </div>

</template>



<script>
export default {

  computed: {

    numCartItems () {
      const numItems = this.$root.$data.numItems
      return numItems
    },
    GetFirstItem () {
    return this.$root.$data.Movies[0]
    },

  },



  }







</script>
<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

#nav {
  padding: 30px;
}

#nav a {
  font-weight: bold;
  color: #2c3e50;
}

#nav a.router-link-exact-active {
  color: #42b983;
}
</style>
