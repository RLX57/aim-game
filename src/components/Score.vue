<template>

  <div class="score" v-if="player">
    {{ score }}
  </div>

</template>

<script>

export default {
  name: 'Score',
  props: ['score', 'player']
}
</script>

<style lang="scss" scoped>

  .score {
    display: block;
    position:absolute;
    bottom:0;
    width:100%;
    height:60px;
    text-align: center;
    font-weight: bold;
    font-size: 25px;
    padding-top: 2vw;
    background-color: #fff8dc;
  }

</style>