<template>
	<v-carousel style="height: 400px !important">
		<v-carousel-item
			v-for="(item, i) in items"
			:key="i"
			:src="item.src"
			reverse-transition="fade-transition"
			transition="fade-transition"
		>
			<v-row
				class="fill-height"
				align="center"
				style="position: relative"
				justify="center"
			>
				<div class="text-h2">{{ item.text }} Slide</div>
			</v-row>
		</v-carousel-item>
	</v-carousel>
</template>
<script>
export default {
	data() {
		return {
			items: [
				{
					src: "https://cdn.vuetifyjs.com/images/carousel/squirrel.jpg",
					text: "test 1",
				},
				{
					src: "https://cdn.vuetifyjs.com/images/carousel/sky.jpg",
					text: "test 2",
				},
				{
					src: "https://cdn.vuetifyjs.com/images/carousel/bird.jpg",
					text: "test 3",
				},
				{
					src: "https://cdn.vuetifyjs.com/images/carousel/planet.jpg",
					text: "test 4",
				},
			],
		};
	},
};
</script>