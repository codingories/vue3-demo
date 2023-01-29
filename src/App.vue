<script setup>
import HeavyComp from "./components/heavyComp.vue";
import {useDefer} from './hooks/useDefer'
const defer = useDefer();
</script>

<template>
  <div class="container">
    <div v-for="n in 100">
<!--      v-if="defer(n)"-->
<!--      v-if="defer(100)"-->
      <HeavyComp v-if="defer(n)"></HeavyComp>
    </div>

<!--    目前画的次数有没有大于一次，没有就是false 实现依次绘制-->
<!--    <HeavyComp v-if="defer(100)"></HeavyComp>-->
<!--    <HeavyComp v-if="defer(200)"></HeavyComp>-->
<!--    <HeavyComp v-if="defer(300)"></HeavyComp>-->

  </div>
</template>

<style scoped>
.container {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  border: 1px solid red;
  grid-gap: 1em;
}
</style>
