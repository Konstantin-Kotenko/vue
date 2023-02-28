<template>
    <button v-bind:type='type'>
        <slot></slot>
    </button>
</template>

<script>
    export default {
        // eslint-disable-next-line vue/multi-word-component-names
        name:'Button',
        props:{
            type:{
                type:String,
                default:'button'
            }
        }
    }
</script>

<style lang="scss" scoped>

</style>