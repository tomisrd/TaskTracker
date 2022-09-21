<template>
    <button @click="onClick()" :style="{background: color}" class="btn">{{text}}</button>
</template>

<script>
    export default {
        name: 'ButtonV',
        props:{
            text: String,
            color: String,
        },
        methods: {
            onClick() {
                this.$emit('btn-click')
            },
        }
    }
</script>