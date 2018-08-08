<template>
	<div>
		<h1>{{ title }}</h1>
		<p>
			<slot></slot>
		</p>
		<ButtonCounter :icon="icon" />
		<button @click="$emit('enlarge-text')">Enlarge Text</button>
		<button @click="$emit('reduce-text')">Reduce Text</button>
	</div>
</template>

<script>
	export default {
		name: 'BlogPost',
		components: {
			ButtonCounter: () => import('@/components/ButtonCounter'),
		},
		props: {
			title: '',
			content: {
				type: String,
				required: true
			},
			icon: ''
		},
		data() {
			return {};
		}
	};
</script>