<template>
	<div class="destinations-table">
		<input type="text" v-model="pickUpLocation" placeholder="From" class="search">
		<input type="text" v-model="dropOffLocation" placeholder="To" class="search">
		<div v-for="destination in filteredDestinations" class="destination">
			<div class="title">
				{{destination.title}}
				<span class="price"> {{destination.price}} </span>
			</div>
		</div>
		<h1> {{points}}</h1>
	</div>
</template>
<script>
	export default {
		name: 'destinations',
		data() {
			return {
				search: '',
				pickUpLocation: '',
				dropOffLocation: '',
				destinations: [
					{
						title: 'Ljubljana - Ljubljana Airport',
						price: '25€',
					},
					{
						title: 'Ljubljana - Trieste Airport',
						price: '100€',
					}
				],
			}
		},
		computed: {
			points: function(){
				return this.pickUpLocation+ '' +this.dropOffLocation;
			},
			filteredDestinations: function(){
				return this.destinations.filter((destination) => {
					return destination.title.match(this.points)
				})
			}
		}
	}
</script>
<style scoped>
	.search{
		width: 200px;
		height: 50px;
		line-height: 50px;
		padding: 0 15px;
		outline: none;
		font-size: 20px;
	}
	.price{
		background: red;
	}
	
</style>