<template>
  <div>
	  <input type="range" min="1" max="5" step="1" value="columnValue" v-model="columnsValue" @change="$emit('columns-value', columnsValue)">
  </div>
</template>

<script>
export default {
	data() {
		return {
			columnsValue: 3
		}
	}
}
</script>

<style lang="scss" scoped>
	input {
		margin: 0px 0px 20px 0px;
	}
</style>