<template>
    <div>
        <!--<input v-model="money">-->
        <input :value="money*factor" v-on:input="handleInput">


    </div>
</template>

<script>
    export default {
        name: "PComponent",
        props: {
            money: Number,
            factor: Number
        },
        methods: {
            handleInput(e) {
                this.$emit('moneyChange', e.target.value/this.factor);
            }
        }
    }
</script>

<style scoped>

</style>
