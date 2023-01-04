<template>
	<main-screen :onChooseSetting="chooseSetting" />
</template>

<script>
	import MainScreen from "./Pages/MainScreen.vue";
	export default {
		name: "App",
		components: {
			"main-screen": MainScreen,
		},
		data: () => {
			return {
				cards: [],
			};
		},
		methods: {
			chooseSetting(setting) {
				this.cards = Array.from(
					{
						length: setting / 2,
					},
					(_, index) => index + 1
				);
				this.cards = [...this.cards, ...this.cards];
				this.cards.sort(() => {
          return Math.floor(Math.random()  -0.5);
        })
			},
		},
	};
</script>

<style>
	#app {
		font-family: Avenir, Helvetica, Arial, sans-serif;
		-webkit-font-smoothing: antialiased;
		-moz-osx-font-smoothing: grayscale;
		text-align: center;
		color: #2c3e50;
		margin-top: 60px;
	}
</style>
