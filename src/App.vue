<script setup>
import NavBar from './components/NavBar.vue'
import FooterAw from './components/FooterAw.vue'
import { ref } from "vue";

const strOne = ref('Hello ');
const strTwo = ref('World');
let getSum = (str, strTwo) => `${str} ${strTwo}`;
</script>

<template>
<NavBar />
<h1>Page</h1>
<p>2+2</p>
<p>{{ getSum(strOne, strTwo) }}</p>
<FooterAw />
</template>

<style scoped>

</style>
