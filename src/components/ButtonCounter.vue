<template>
	<div class="component">
		<button @click="counter++">{{ icon }} ({{ display }}) {{ counter }}</button>
	</div>
</template>

<script>
	export default {
		name: 'ButtonCounter',
		props: {
			icon: ''
		},
		data() {
			return {
				counter: 0
			};
		},
		computed: {
			display: function() {
				return this.counter > 0 ? "+" : "-";
			}
		}
	};
</script>

<style scoped="">
	.component {
		display: plex;
	}
	button {
		margin: 2px;
		padding: 5px;
		border-color: blue;
		border-width: 2px;
		background-color: white;
		border-radius: 15%;
		min-width: 5em;
		min-height: 2em;
		font-size: 20px;
	}
</style>