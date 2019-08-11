<template>
	<div id="app">
<!--		<search></search>-->
		<destinations></destinations>
	</div>
</template>

<script>
	import Search from './components/Search'
	import Destinations from './components/Destinations'

	export default {
		name: 'App',
		components: {
			Search, Destinations,
		}
	}
</script>

<style>
	#app {
		font-family: 'Avenir', Helvetica, Arial, sans-serif;
		-webkit-font-smoothing: antialiased;
		-moz-osx-font-smoothing: grayscale;
		text-align: center;
		color: #2c3e50;
		margin-top: 60px;
	}
</style>