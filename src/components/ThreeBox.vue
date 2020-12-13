<template>
	<div class="row">
		<div class="column">
			<div class="image">
				<img src="@/assets/01.jpg" alt="">
			</div>
		</div>
		<div class="column">
			<div class="image">
				<img src="@/assets/01.jpg" alt="">
			</div>
		</div>
		<div class="column">
			<div class="image">
				<img src="@/assets/01.jpg" alt="">
			</div>
		</div>
	</div>
</template>

<style lang="scss" scoped>
	.column {
		flex: 0 1 33.333%;
		@media (max-width:710px){
			flex: 0 1 50%;			
		}
		@media (max-width:470px){
			flex: 1 1 100%;			
		}
	}
</style>