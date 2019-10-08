<template>
	<div>
		<h1>Follow Along</h1>

		<div :style="{ 'font-size': `${this.postFontSize}em` }">
			<BlogPost
				v-for="blog in blogs"
				:title="blog.title"
				:icon="blog.icon"
				:content="blog.content"
				
				:key="blog.id"
				@enlarge-text="increaseFontSize"
				@reduce-text="decreaseFontSize">
					{{ blog.content }}
				</BlogPost>
		</div>
	</div>
</template>

<script>
	export default {
		name: 'FollowAlong',

		components: {
			BlogPost: () => import ('@/components/BlogPost')
		},

		data() {
			return {
				postFontSize: 0.8,
				blogs: [
					{
						id: 1,
						title: 'Component Design',
						content: 'Lorem ipsum dolor sit amet, consectetur adipisicing elit. Molestias, consequatur quis fuga modi tempore officia nostrum dolorum incidunt ipsa eos.',
						icon: '👍'
					},
					{
						id: 2,
						title: 'API Call',
						content: 'Lorem ipsum dolor sit amet, consectetur adipisicing elit. Magni, mollitia atque perspiciatis ipsum ea quas sapiente quam reprehenderit distinctio autem.',
						icon: '❤️'
					},
					{
						id: 3,
						title: 'Introduction to Vuex',
						content: 'Lorem ipsum dolor sit amet, consectetur adipisicing elit. Placeat tempore repellendus ut molestias cumque asperiores dicta, praesentium doloribus cupiditate quasi.',
						icon: '🔥'
					},
				]
			}
		},
		computed: {
			size: function() {
				return `${this.postFontSize}em`
			},
		},
		methods: {
			increaseFontSize() {
				return this.postFontSize += 0.1;
			},
			decreaseFontSize() {
				return this.postFontSize -= 0.1;
			}
		}
	};
</script>
