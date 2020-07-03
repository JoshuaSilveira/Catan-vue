<template>
  <div>
    <p class="value">{{num}}</p>
    <p class="rarity" v-bind:class="changeTokenColor()">{{getrarity()}}</p>
  </div>
</template>

<script>
export default {
  name: "Token",
  props: ["num"],
  methods: {
    getrarity() {
      if (this.num === 2 || this.num === 12) {
        return "*";
      } else if (this.num === 3 || this.num === 11) {
        return "**";
      } else if (this.num === 4 || this.num === 10) {
        return "***";
      } else if (this.num === 5 || this.num === 9) {
        return "****";
      } else if (this.num === 6 || this.num === 8) {
        return "*****";
      }
    },
    changeTokenColor() {
      return { eight: this.num === 8,six: this.num === 6, };
    }
  }
};
</script>

<style scoped>
.value {
  text-align: center;
  font-size: 1.4em;
  font-weight: bold;
  color: white;
  text-shadow: 2px 2px #000000;
}
.rarity {
  text-align: center;
  font-size: 1.4em;

  color: white;
}
.eight {
  color: red;
}
.six {
  color: red;
}
</style>