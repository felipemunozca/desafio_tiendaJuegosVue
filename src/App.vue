<template>
  <div id="app">
    <nav class="navbar bg-dark border-bottom border-bottom-dark" data-bs-theme="dark">
      <div class="container-fluid">
        <a class="navbar-brand" href="#">Tienda Bit-Game</a>
        <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNavAltMarkup" aria-controls="navbarNavAltMarkup" aria-expanded="false" aria-label="Toggle navigation">
          <span class="navbar-toggler-icon"></span>
        </button>
      </div>
    </nav>

    <ListadoJuegos :games="games" @eliminarJuego="eliminarJuegoPadre" />
  </div>
</template>

<script>

import ListadoJuegos from '@/components/ListadoJuegos.vue';

export default {
  name: 'App',
  components: {
    ListadoJuegos,
  },
  data() {
    return {
      games: ["Arena of valor", "Pokemon Unite", "Donkey Kong", "Heroes of the storm", "Valorant"]
    }
  },
  methods: {
    eliminarJuegoPadre(id) {
      this.games.splice(id, 1)
    }
  },
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  /* text-align: center; */
  color: #2c3e50;
  /* margin-top: 60px; */
}
</style>
