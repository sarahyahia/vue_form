<template>
    <header>
        <h1>{{ title }}</h1>
    </header>
</template>
<script>
export default{
    name: 'Header',
    props:{
        title: String,
    }
}
</script>
<style scoped>
    header {
        display: flex;
        margin: 5%;
    }
</style>