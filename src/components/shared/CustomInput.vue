<template>
    <input 
    :value="modelValue"
    @input="$emit('update:modelValue', $event.target.value)"
    class="custom-input"
/>
</template>

<script>
export default {
  props: ['modelValue'],
  emits: ['update:modelValue']
}
</script>

<style lang="scss" scoped>
.custom-input {
    min-height: 40px;
    border: 2px solid #FF662D;
    font-size: 18px;
    outline: none;
    line-height: inherit;
    padding: 9px 15px;
}
</style>
