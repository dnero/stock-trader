<template>
	<div>
		<app-stock v-for="stock in stocks"></app-stock>
	</div>
</template>

<script>
	import {mapGetters} from 'vuex';
	import Stock from './Stock.vue';

	export default {
		computed: {
			stocks() {
				return this.$store.getters.stockPortfolio;
			}
			// mapGetters({
			// 	stocks: 'stockPortfolio'
			// })
		},
		components: {
			appStock: Stock
		}
	}
</script>