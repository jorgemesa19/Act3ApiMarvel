<template>
  <v-app>
    <!-- <v-div id="app">
      <v-div id="nav">
        <img src="../assets/marvel.png">
      </v-div>
      <v-List/>
    </v-div> -->

    <v-main>
      <v-container>
        <Nuxt />
      </v-container>
    </v-main>

    <v-footer>
      <span>&copy; {{ new Date().getFullYear() }}</span>
    </v-footer>
  </v-app>
</template>

<script>
export default {
  name: 'DefaultLayout',
  data() {
    return {
      title: 'MARVEL',
    }
  },
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  background-color: white;
}

img{
  width: 100%;
  height: 300px;
  size: cover;
  border: 10px solid white;
  margin-top: 10px;
  align-items: center;
}
</style>

