<template>
    <div>
        <select
        @change='onChange()'
         v-model='selected' class="form-select mt-10 block w-full border p-3 rounded shadow bg-blue-100">
            <Option value="0">Select Country</Option>
            <Option v-for='country in countries' :value="country.ID">{{country.Country}}</Option>
        </select> 
    </div>
</template>

<script>
    export default {
        name: 'CountrySelect',
        props: ['countries'],
        data() {
            return {
                selected: 0
            }
        },
        methods: {
            onChange() {
                const country = this.countries.find((item) => item.ID === this.selected)
                this.$emit('get-country' , country)
            }
        },
    }
</script>