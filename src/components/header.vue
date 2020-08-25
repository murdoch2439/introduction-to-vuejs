<template>
    <div id="header">
        <h1>{{title}}</h1>
        <p>{{desc}}</p>
    </div>
</template>

<script>
export default {
    name:"Header",
    props:["title", "desc"]
};
</script>

<style>
    #header{
        background:#ccc;
        padding:2rem;

    }
</style>