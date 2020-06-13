<template>
    <div>
        <app-stock v-for="stock in stocks" :key="stock" :stock="stock"></app-stock>
    </div>
</template>

<script>
import {mapGetters} from 'vuex';
import Stock from './Stock.vue';

export default {
    computed:{
        ...mapGetters({
            stocks: 'stockPortfolio',
            funds:'funds'
        })
    },
    components: {
        appStock: Stock
    }
}
</script>