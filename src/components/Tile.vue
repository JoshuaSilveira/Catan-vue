<template>
  <div v-bind:class="getClass()" class="hex">
    <p>{{tile.token}}</p>
  </div>
</template>

<script>
export default {
  name: "Tile",
  props: ["tile"],
  methods: {
    getClass() {
      return {
        desert: this.tile.type === "desert",
        mountain: this.tile.type === "mountain",
        field: this.tile.type === "field",
        forest: this.tile.type === "forest",
        hills: this.tile.type === "hills"
      };
    }
  }
};
</script>
<style scoped>
.hex:before {
  content: " ";
  width: 0;
  height: 0;
  border-bottom: 30px solid #6c6;
  border-left: 52px solid transparent;
  border-right: 52px solid transparent;
  position: absolute;
  top: -30px;
}

.hex {
  margin-top: 30px;
  width: 104px;
  height: 60px;
  background-color: #6c6;
  position: relative;
}
.hex p {
  text-align: center;
  font-size: 1.4em;
  font-weight: bold;
  color: white;
  text-shadow: 2px 2px #000000;
}
.hex:after {
  content: "";
  width: 0;
  position: absolute;
  bottom: -30px;
  border-top: 30px solid #6c6;
  border-left: 52px solid transparent;
  border-right: 52px solid transparent;
}

.forest {
  background-color: rgb(2, 75, 2);
}
.forest:before {
  border-bottom: 30px solid rgb(2, 75, 2);
}
.forest:after {
  border-top: 30px solid rgb(2, 75, 2);
}

.hills {
  background-color: rgb(238, 89, 2);
}
.hills:before {
  border-bottom: 30px solid rgb(238, 89, 2);
}
.hills:after {
  border-top: 30px solid rgb(238, 89, 2);
}

.field {
  background-color: rgb(255, 176, 5);
}
.field:before {
  border-bottom: 30px solid rgb(255, 176, 5);
}
.field:after {
  border-top: 30px solid rgb(255, 176, 5);
}

.mountain {
  background-color: rgb(44, 35, 29);
}
.mountain:before {
  border-bottom: 30px solid rgb(44, 35, 29);
}
.mountain:after {
  border-top: 30px solid rgb(44, 35, 29);
}

.desert {
  background-color: rgb(223, 145, 94);
}
.desert:before {
  border-bottom: 30px solid rgb(223, 145, 94);
}
.desert:after {
  border-top: 30px solid rgb(223, 145, 94);
}
</style>