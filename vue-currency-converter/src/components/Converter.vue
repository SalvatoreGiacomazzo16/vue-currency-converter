<script setup>
import { ref, onMounted } from 'vue';
import axios from 'axios';
import CurrencyInput from './CurrencyInput.vue';

const currencies = ref({});

const defaultSelect1 = ref('EUR');
const defaultSelect2 = ref('USD');

//Api Call
onMounted(async () => {  
try {
    const response = await axios.get('https://api.frankfurter.app/currencies');
    currencies.value = response.data;
    console.log("Api Call Success.", response.data);

} catch (error){
    console.error("Failed Api Call.", error);
}
});


</script>

<template>
    <div class="container box">
<h1 class="text-center"> Currency Converter</h1>

<CurrencyInput
:currencies = "currencies"
  :defaultSelect1="defaultSelect1"
      :defaultSelect2="defaultSelect2"

/>

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
