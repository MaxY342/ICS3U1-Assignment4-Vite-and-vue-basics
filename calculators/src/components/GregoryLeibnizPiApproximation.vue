<script setup>
import { ref } from 'vue';

const nValue = ref(0);
const result = ref(0);

function piApproximation() {
    let output = 0
    for (let i = 0; i < nValue.value; i++) {
        output += Math.pow(-1, i) / (2 * i + 1)
    }
    result.value = 4 * output;
}
</script>

<template>
  <form @submit.prevent="piApproximation()">
    <h1>Gregory-Leibniz Pi Approximation</h1>
    <label>n Value:</label>
    <input type="number" v-model="nValue" />
    <label>Pi Approximation (Result):</label>
    <input readonly v-model="result" />
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