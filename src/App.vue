<template>
  <div id="app" class="container">
    <h1 class="text-center m-5">Player Score Counter</h1>
    <div class="card">
      <div class="card-body text-center">
        <h3>Player 1</h3>
        <div class="d-flex align-items-center m-auto">
          <button @click="decreaseCounter(player_1)" type="button" class="btn btn-danger">Down</button>
          <span class="player-score m-5">{{player_1.score}}</span>
          <button @click="increaseCounter(player_1)" type="button" class="btn btn-success">Up</button>
        </div>
      </div>
    </div>
    <div class="card">
      <div class="card-body text-center">
        <h3>Player 2</h3>
        <div class="d-flex align-items-center m-auto">
          <button @click="decreaseCounter(player_2)" type="button" class="btn btn-danger">Down</button>
          <span class="player-score m-5">{{player_2.score}}</span>
          <button @click="increaseCounter(player_2)" type="button" class="btn btn-success">Up</button>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      player_1: {
        score: 0,
      },
      player_2: {
        score: 0,
      },
    };
  },
  methods: {
    increaseCounter(player) {
      player.score += 1;
    },
    decreaseCounter(player) {
      if (player.score > 0) {
        player.score -= 1;
      }
    },
  },
};
</script>

<style>
.player-score {
  font-size: 2em;
}
.card-body div:first-child {
  width: fit-content;
  width: -moz-fit-content;
}
</style>
