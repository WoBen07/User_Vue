<template>
    <div>
        <h2>{{ name }}</h2>
        <h3>{{ age }}</h3>
    </div>
    
</template>
<script>
    export default {
        emits: ['delete'],
        props: {
            id: {
                type: String,
                required: true
            },
            name: {
                type: String,
                required: true
            },
            age: {
                type: String,
                required: true
            }
        },
        methods: {
            
        }
    }
</script>
<style scoped>
 div {
    display: flex;
    align-items: center;
    justify-content: center;
    flex-direction: column;
    background-color: grey;
    border: 2px solid black;
 }
</style>
