<template>
  <div class="item-container">
    <div v-for="n in 4000" class="item">

    </div>
  </div>
</template>

<script>
export default {

}
</script>
<style>
.item-container {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  border: 1px solid yellowgreen;
}
.item {
  width: 5px;
  height: 3px;
  background-color: #ccc;
  margin: .1em;
}
</style>
