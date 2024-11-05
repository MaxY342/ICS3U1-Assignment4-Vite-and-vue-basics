<script setup>
import { ref } from 'vue';

const mValue = ref(0);
const nValue = ref(0);
const asymptoteType = ref(0);

function asymptote() {
    if (mValue.value == nValue.value) {
        asymptoteType.value = "The asymptote is horizontal";
    }
    else if (nValue.value > mValue.value) {
        asymptoteType.value = "The asymptote is the x-axis";
    }
    else {
        switch(mValue.value - nValue.value) {
            case 1:
                asymptoteType.value = "Linear";
                break;
            case 2:
                asymptoteType.value = "Quadratic";
                break;
            case 3:
                asymptoteType.value = "Cubic";
                break;
            case 4:
                asymptoteType.value = "Quartic";
                break;
            case 5:
                asymptoteType.value = "Quintic";
                break;
            case 6:
                asymptoteType.value = "Sextic";
                break;
            case 7:
                asymptoteType.value = "Septic";
                break;
            case 8:
                asymptoteType.value = "Octic";
                break;
            case 9:
                asymptoteType.value = "Nonic";
                break;
            case 10:
                asymptoteType.value = "Decic";
                break;
        }
    }
}
</script>

<template>
  <form @submit.prevent="asymptote()">
    <h1>Asymptote Finder</h1>
    <label>m Value:</label>
    <input type="number" v-model="mValue" />
    <label>n Value:</label>
    <input type="number" v-model="nValue" />
    <label>Asymptote Type (Result):</label>
    <input readonly v-model="asymptoteType" />
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