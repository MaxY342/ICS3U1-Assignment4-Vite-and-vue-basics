<script setup>
import { ref } from 'vue';

const sideA = ref(0);
const sideB = ref(0);
const angleC = ref(0);
const sideC = ref(0);

function cosineLaw() {
  let angleCRadians = angleC.value * (Math.PI / 180);
  sideC.value = Math.sqrt(Math.pow(sideA.value, 2) + Math.pow(sideB.value, 2) - (2 * sideA.value * sideB.value) * Math.cos(angleCRadians));
}
</script>

<template>
  <form @submit.prevent="cosineLaw()">
    <h1>Cosine Law</h1>
    <label>Side a:</label>
    <input type="number" step="any" v-model="sideA" />
    <label>Side b:</label>
    <input type="number" step="any" v-model="sideB" />
    <label>Angle c:</label>
    <input type="number" step="any" v-model="angleC" />
    <label>Side c (Result):</label>
    <input readonly v-model="sideC" />
    <button type="submit">Calculate</button>
  </form>
</template>

<style scoped>
form {
    display: flex;
    flex-direction: column;
    padding: 2rem;
    border-radius: 10px;
    box-shadow: 0px 8px 16px 0px rgba(0,0,0,0.2);
    width: 50vh;
}

h1 {
    text-align: center;
}

button {
    background-color: #067fdf;
    margin: 30px;
    padding: 1rem;
    color: white;
    border: 0;
    border-radius: 10px;
}

button:hover {
    background-color: #0c85e5;
    cursor: pointer;
}

label {
    font-size: 20px;
    margin-top: 1rem;
    margin-bottom: 1rem;
}

input {
    height: 2rem;;
}
</style>