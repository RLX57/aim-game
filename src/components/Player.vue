<template>

  <div class="text-center">
    <span v-html="message" :class="{ hide: !player }"></span>
    <form @submit.prevent="startGame" :class="{ hide: player }">
      <input name="player" placeholder="Entrez un pseudo"/>
      <button type="submit">Jouer</button>
    </form>
  </div>

</template>

<script>

export default {
  name: 'Player',
  data() {
    return {
      player: '',
      message: ''
    }
  },
  updated() {
    this.message = `Bonjour <span class="player">${this.player}</span> ! `
  },
  methods: {
    startGame(event) {
      let name = event.target[0].value

      if(!name) {
        alert('Renseignez un pseudo')
        return
      }

      this.player = name
      this.$emit('player')
    }
  },
}
</script>

<style lang="scss" scoped>

.hide {
  display: none;
}

.text-center{
  text-align: center;
}

</style>