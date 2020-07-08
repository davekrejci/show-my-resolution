<template>
	<div id="app">{{ this.width }} x {{ this.height }}</div>
</template>

<script>
export default {
	name: 'App',
	data() {
		return {
			width: window.innerWidth,
			height: window.innerHeight
		};
	},
	created() {
		window.addEventListener('resize', this.getDimensions);
	},
	methods: {
		getDimensions() {
			this.width = window.innerWidth;
			this.height = window.innerHeight;
		}
	}
};
</script>

<style>
html,
body {
	margin: 0;
	padding: 0;
	height: 100%;
}
#app {
	font-family: Avenir, Helvetica, Arial, sans-serif;
	-webkit-font-smoothing: antialiased;
	-moz-osx-font-smoothing: grayscale;
	display: flex;
	justify-content: center;
	align-items: center;
	color: #333;
	font-size: 15vw;
	font-weight: bold;
	margin: 0px;
	height: 100%;
	width: 100%;
	background-color: rgb(214, 153, 40);
}
</style>
