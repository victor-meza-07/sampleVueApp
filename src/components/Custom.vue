<template>
    <h1>{{greeting}}</h1>
</template>

<script>
export default {
    name: 'Custom',
    props: {
        greeting: String
    }
}
</script>


<style scoped>
    h1{
        color:red;
        font-size: 100px;
        font-family:'Times New Roman';
    }
</style>
