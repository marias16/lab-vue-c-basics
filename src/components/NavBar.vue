<script setup>
import { reactive } from "vue";
const title = true;
const posts = reactive([
    {title:'Simplify',
    description:'This is Simplify article',
    content: 'The content contains things',
    },
    {title:'Dashcoin',
    description:'This is Dashcoin article',
    content: 'Dashcoin sounds like a bitcoin',
    },
    {title:'Vectorify',
    description:'A Design project',
    content: 'joel did nothing wrong',
    }
])
</script>

<template>

<ul>
    <li>Home</li>
    <li>About Us</li>
    <li>Contact Us</li>
</ul>
<h1 v-if="title">Title</h1>
<h1>Posts</h1>
<div class="container">
    <div v-for="post in posts" :key="post.title">
        <h3>{{ post.title }}</h3>
        <h4>{{ post.description }}</h4>
        <p>{{ post.content }}</p>
    </div>
</div>
</template>

<style scoped>
    ul {
        display: flex;
        list-style: none;
        gap: 1em;
    }

    .container {
        display: flex;
        gap: 5px;
    }

    h3 {
        background-color: beige;
    }
</style>