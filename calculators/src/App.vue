<script setup>
import CosineLaw from './components/CosineLaw.vue';
import Asymptote from './components/Asymptote.vue';
import GregoryLeibnizPiApproximation from './components/GregoryLeibnizPiApproximation.vue';
</script>

<template>
  <div class="app-container">
    <CosineLaw />
    <Asymptote />
    <GregoryLeibnizPiApproximation />
  </div>
</template>

<style scoped>
.app-container {
    display: grid;
    grid-template-columns: 45vw 45vw;
    gap: 100px;
}
</style>