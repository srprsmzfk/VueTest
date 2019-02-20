<template>
    <div>
    <input :value="money" v-on:input="handleInput">
    </div>
</template>

<script>
    export default {
        name: "DComponent",
        props: {
            money: Number
        },
        methods: {
            handleInput(e) {
                this.$emit('moneyChange', e.target.value);
            }
        }
    }
</script>

<style scoped>

</style>
