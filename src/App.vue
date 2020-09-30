<template>
  <div id="app">
    <Score :score="score" :player="player"></Score>
    <Player v-on:player="updatePlayer" class="text-center"></Player>
  </div>
</template>

<script>
import Score from './components/Score'
import Player from './components/Player'

export default {
  name: 'App',
  data() {
    return {
      score: 0,
      player: false
    }
  },
  components: {
    Score,
    Player
  },
  methods: {
    updateScore(score) {
      this.score = score
    },
    updatePlayer() {
      this.player = true
    }
  }
}
</script>

<style lang="scss">

  #app {
    font-family: Avenir, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    width: 100vw;
    height: 60vh;
    display: block;
  }
</style>
