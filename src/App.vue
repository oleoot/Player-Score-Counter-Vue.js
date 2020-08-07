<template>
  <div id="app" class="container">
    <h1 class="text-center">Player Score Counter</h1>
    <div class="card">
      <div class="card-body text-center">
        <h3>Player 1</h3>
        <button @click="decreaseCounter" type="button" class="btn btn-danger">Down</button>
        <span class="player-score">{{player_1_score}}</span>
        <button @click="increaseCounter" type="button" class="btn btn-success">Up</button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      player_1_score: 0,
    };
  },
  methods: {
    increaseCounter() {
      this.player_1_score += 1;
    },
    decreaseCounter() {
      this.player_1_score -= 1;
    },
  },
};
</script>

<style>
.player-score {
  font-size: 2em;
}
</style>
