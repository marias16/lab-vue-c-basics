<script setup>
import NavBar from './components/NavBar.vue'
import FooterAw from './components/FooterAw.vue'
import { ref } from "vue";

const strOne = ref('Hello ');
const strTwo = ref('World');
let getSum = (str, strTwo) => `${str} ${strTwo}`;

//button  css logic
let blueActive = ref(false);
let getActive = () => blueActive.value = true;
</script>

<template>
<div :class="{ blue : blueActive }"> This is my page! </div>
<button @click="getActive">Click Me</button>
<NavBar />
<h1>Page</h1>
<p>2+2</p>
<p>{{ getSum(strOne, strTwo) }}</p>
<FooterAw />
</template>

<style scoped>

div {
    background-color: green;
    width: 100%;
}

.blue {
    background-color: blue;
}

</style>
