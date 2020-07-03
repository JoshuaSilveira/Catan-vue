<template>
  <div class="legend">
    <h2>Legend</h2>
    <div>
      Pasture:
      <div class="block pasture"></div>
    </div>
    <div>Field: <div class="block field"></div></div>
    <div>Hills: <div class="block hills"></div></div>
    <div>Mountain: <div class="block mountain"></div></div>
    <div>Forest: <div class="block forest"></div></div>
    <div>Desert: <div class="block desert"></div></div>
  </div>
</template>
<script>
export default {};
</script>
<style scoped>
.legend {
  
  text-align: left;
  padding-right: 20%;
}
.block{
  display: inline-block;
  width: 20px;
  height: 20px;
  
}
.pasture {
 
  background-color: #6c6;
}
.forest {
 
  background-color: rgb(2, 75, 2);
}
.mountain {
  
  background-color: rgb(44, 35, 29);
}
.desert {
  
  background-color: rgb(223, 145, 94);

}
.hills {
  
  background-color: rgb(238, 89, 2);
}
.field {
  
  background-color: rgb(255, 176, 5);
}
</style>