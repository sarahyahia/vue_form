<template>
    <button class="btn" :style="{background:color}" type="submit">{{ text }}</button>
</template>

<script>
    export default{
        name: 'Button',
        props: {
            text:String,
            color:String,
        },
        methods: {
           
        }
    }
</script>
