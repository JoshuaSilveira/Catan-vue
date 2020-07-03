<template>
  <div id="app">
    <Board v-bind:tiles="tiles" />
  </div>
</template>

<script>
import Board from "./components/Board";
export default {
  name: "App",
  components: {
    Board
  },
  created() {
    this.generateTiles();
  },
  methods: {
    generateTiles: function() {
      var tiles = [];
      var tokenVal = [
        2,
        3,
        3,
        4,
        4,
        5,
        5,
        6,
        6,
        8,
        8,
        9,
        9,
        10,
        10,
        11,
        11,
        12,
        12
      ];
      var terrainTypes = [
        "forest",
        "forest",
        "forest",
        "forest",
        "pasture",
        "pasture",
        "pasture",
        "pasture",
        "field",
        "field",
        "field",
        "field",
        "hills",
        "hills",
        "hills",
        "mountain",
        "mountain",
        "mountain",
        "desert"
      ];

      for (var i = 0; i <= 18; i++) {
        var tileToken;
        var randomNum = Math.floor(Math.random() * terrainTypes.length);
        var tileTerrain = terrainTypes[randomNum];
        terrainTypes.splice(randomNum, 1);
        if (tileTerrain === "desert") {
          tileToken = "";
        } else {
          tileToken = tokenVal[randomNum];
          tokenVal.splice(randomNum, 1);
        }
        
        var tile = {
          id: i,
          type: tileTerrain,
          token: tileToken
        };
        tiles.push(tile);
      }
      this.tiles = tiles;
    }
  },

  data() {
    return {
      tiles: []
    };
  }
};
</script>

<style></style>
