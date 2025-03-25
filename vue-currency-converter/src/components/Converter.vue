<script setup>
import axios from 'axios';
import CurrencyInput from './CurrencyInput.vue';



</script>

<template>
    <div class="container box">
<h1 class="text-center"> Currency Converter</h1>

<CurrencyInput />

</div>
</template>

<style lang="scss">
.box{
    border-color: orange;
}
h1{
    color:orange;
}

</style>
