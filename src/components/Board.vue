<template>
  <div >
    <img
      class="boundary"
      src="https://alexbeals.com/projects/catan/assets/images/background.png"
      alt
    />
    <div class="board">
      <div class="hex-row">
        <div v-bind:key="tile.id" v-for="tile in tiles.slice(0,3)">
          <div class="tile">
            <Tile v-bind:tile="tile" />
          </div>
        </div>
      </div>
      <div class="hex-row even">
        <div v-bind:key="tile.id" v-for="tile in tiles.slice(3,7)">
          <div class="tile">
            <Tile v-bind:tile="tile" />
          </div>
        </div>
      </div>
      <div class="hex-row odd">
        <div v-bind:key="tile.id" v-for="tile in tiles.slice(7,12)">
          <div class="tile">
            <Tile v-bind:tile="tile" />
          </div>
        </div>
      </div>
      <div class="hex-row even">
        <div v-bind:key="tile.id" v-for="tile in tiles.slice(12,16)">
          <div class="tile">
            <Tile v-bind:tile="tile" />
          </div>
        </div>
      </div>
      <div class="hex-row">
        <div v-bind:key="tile.id" v-for="tile in tiles.slice(16,19)">
          <div class="tile">
            <Tile v-bind:tile="tile" />
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Tile from "./Tile";
export default {
  name: "Board",
  components: {
    Tile
  },
  props: ["tiles"]
};
</script>

<style scoped>
.hex-row {
  clear: left;
  margin-left: 106px;
  
}
.tile {
  float: left;
  margin-left: 3px;
  margin-bottom: 3px;
}
.even {
  margin-left: 53px;
  
}
.odd {
  margin-left: 0px;
  
}
.boundary {
  width: 724px;
  position: absolute;
  top: 223px;
  left:247px;
 
  z-index: -1;
}
.board{
    position: relative;
    top: 83px;
    left:333px

}

</style>