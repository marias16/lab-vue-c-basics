<script setup>
const title = true;
</script>

<template>
<ul>
    <li>Home</li>
    <li>About Us</li>
    <li>Contact Us</li>
</ul>
<h1 v-if="title">Title</h1>
</template>

<style scoped>
    ul {
        display: flex;
        list-style: none;
        gap: 1em;
    }
</style>