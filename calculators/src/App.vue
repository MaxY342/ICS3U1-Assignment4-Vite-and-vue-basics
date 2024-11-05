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
  display: flex;
  gap: 2rem;
}
</style>