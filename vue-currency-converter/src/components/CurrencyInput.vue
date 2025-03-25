<template>
    <div class="currency-input row g-1 mt-5">
        <div class="col-md-6">
  
  <input type="text" class="form-control input-field" placeholder="Number" aria-label="Number" aria-describedby="Number">
</div>
<div class="col-md-6">
        <select class="form-select input-field" aria-label="Default select example">
            <option selected value="1">One</option>
            <option value="2">Two</option>
            <option value="3">Three</option>
       </select>
    </div>
    </div>

    <div class="currency-input row g-1 mt-5">
        <div class="col-md-6">
  
  <input type="text" class="form-control input-field" placeholder="Number" aria-label="Number" aria-describedby="Number">
</div>
<div class="col-md-6">
        <select class="form-select input-field" aria-label="Default select example">
            <option selected value="1">One</option>
            <option value="2">Two</option>
            <option value="3">Three</option>
       </select>
    </div>
    </div>

</template>

<script>
export default {
    name: 'CurrencyInput',
    props: {
       
    },
    data() {
        return {
          
        };
    },
    methods: {
       
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