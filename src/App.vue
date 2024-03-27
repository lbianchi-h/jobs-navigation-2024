<template>
  <nav>
    <router-link to="/">Home</router-link> |
    <router-link to="/about">About</router-link> |
    <router-link to="/jobs">Jobs</router-link>
  </nav>

  <button v-on:click="redirect">Redirect</button>
  <button v-on:click="back">Back</button>
  <button v-on:click="forward">Forward</button>

  <router-view/>
</template>

<script>

export default ({
  methods: {
    redirect() {
      this.$router.push( { name: 'home' } )
    },
    back() {
      this.$router.go(-1) /* Permet de reculer d'un cran dans l'historique */
    },
    forward() {
      this.$router.go(1) /* Avance d'un pas */
    }
  }
})
</script>


<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

nav {
  padding: 30px;
}

nav a {
  font-weight: bold;
  color: #2c3e50;
}

nav a.router-link-exact-active {
  color: #42b983;
}

button {
  margin: 0 10px;
  padding: 20 px;
  border: none;
  border-radius: 4px;
}
</style>
