<template>

   <div class="currency-input row g-1 mt-5">
        <div class="col-md-6">
  
  <input type="text" class="form-control input-field" placeholder="Amount" v-model="select1" @input="validateNumber('select1')" >
</div>
<div class="col-md-6">
    <select class="form-select input-field"  v-model="selectedCurrency1" aria-label="Default select example">
            <option 
          v-for="(currencyName, currencyCode) in currencies" 
          :key="currencyCode" 
          :value="currencyCode"
        >
          {{ currencyCode }} - {{ currencyName }}
        </option>
    </select>
    </div>
    </div>

    <div class="currency-input row g-1 mt-5">
        <div class="col-md-6">
  
  <input type="text" class="form-control input-field" placeholder="Amount" v-model="select2" @input="validateNumber('select2')" >
</div>
<div class="col-md-6">
        <select class="form-select input-field"  v-model="selectedCurrency2" aria-label="Default select example">
            <option 
          v-for="(currencyName, currencyCode) in currencies" 
          :key="currencyCode" 
          :value="currencyCode"
          
        >
          {{ currencyCode }} - {{ currencyName }}
        </option>
       </select>
    </div>
    </div>


</template>

<script>
export default {
    name: 'CurrencyInput',
    props: {
        currencies: {
      type: Object,
      required: true
    },
    defaultSelect1: {
      type: String,
      default: 'EUR'
    },
    defaultSelect2: {
      type: String,
      default: 'USD'
    }
        
       
    },
    data() {
        return {
            selectedCurrency1: this.defaultSelect1,
      selectedCurrency2: this.defaultSelect2,
      select1: "",
      select2: "",
          
        };
    },
    methods: {
      validateNumber(field) {
      
         if (field === 'select1') {
            this.select1 = this.select1.replace(/[^\d.]/g, '');
        } else if (field === 'select2') { 
            this.select2 = this.select2.replace(/[^\d.]/g, '');
        }
     
    this[field] = this[field].replace(/[^\d.]/g, '');
  }
       
    },
    computed: {
        
    },
};
</script>

<style scoped>
.input-field{
    background-color: orange;
}
.input-field:hover {
    background-color: darkorange;
}

.input-field:focus {
    box-shadow: 0 0 0 0.25rem rgb(195, 93, 24);
}
</style>