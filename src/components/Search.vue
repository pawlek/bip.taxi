<template>
	<div class="search">
		<input type="text" v-model="search" placeholder="search place">
	</div>
</template>
<script>
	export default {
		name: 'search',
		data() {
			return {
				search: '',
				destinations: []
			}
		},
		computed: {
			filteredDestinations: function(){
				return this.destinations.filter((destination) => {
					return destination.title.match(this.search)
				})
			}
		}
	}
</script>
<style scoped>
	
</style>