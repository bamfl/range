<template>
  <div class="container">
	  <Range @columns-value="Value" />
	  
	  <OneBox v-model="columnsNumber" v-if="columnsNumber == 1" />

	  <TwoBox v-else-if="columnsNumber == 2" />

	  <ThreeBox v-else-if="columnsNumber == 3" />

	  <FourBox v-else-if="columnsNumber == 4" />

	  <FiveBox v-else-if="columnsNumber == 5" />
  </div>
</template>

<script>
import Range from '@/components/Range'
import OneBox from '@/components/OneBox'
import TwoBox from '@/components/TwoBox'
import ThreeBox from '@/components/ThreeBox'
import FourBox from '@/components/FourBox'
import FiveBox from '@/components/FiveBox'

export default {
	data() {
		return {
			columnsNumber: 3
		}
	},
	components: {
		Range,
		OneBox, TwoBox, ThreeBox, FourBox, FiveBox
	},
	methods: {
		Value(columnsValue) {
			console.log(columnsValue);
			this.columnsNumber = columnsValue
		}
	}
}
</script>

<style lang="scss">
	.container {
		max-width: 1200px;
		padding: 0 15px;
		margin: 0 auto;
	}
	.row {
		display: flex;
		justify-content: center;
		flex-wrap: wrap;
		margin: 0 -20px;
	}

	.column {
		padding: 0 20px;
		margin: 0px 0px 20px 0px;
	}

	.image {
		position: relative;
		height: 300px;
		min-width: 200px;
		
		img {
			position: absolute;
			width: 100%;
			height: 100%;
			top: 0;
			left: 0;
			object-fit: cover;
		}
	}
</style>