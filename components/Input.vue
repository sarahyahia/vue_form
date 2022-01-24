<template>
    <input :type="type"  :name="name" :id="id">
</template>

<script>
    export default{
        name: 'Input',
        props: {
            type:String,
            name:String,
            id:String,
        }
    }
</script>
<style scoped>
    input {
        height: 30px;
        padding: 5px;
        display: block;
        margin-bottom: 1%;
    }
</style>