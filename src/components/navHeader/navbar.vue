<template>
	<div>
		<v-app-bar color="" dark prominent style="height: auto">
			<v-app-bar-nav-icon
				@click.stop="drawer = !drawer"
			></v-app-bar-nav-icon>

			<v-btn icon>
				<v-icon>mdi-magnify</v-icon>
			</v-btn>

			<v-btn icon>
				<v-icon>mdi-filter</v-icon>
			</v-btn>

			<v-btn icon>
				<v-icon>mdi-dots-vertical</v-icon>
			</v-btn>
		</v-app-bar>
		<v-navigation-drawer
			v-model="drawer"
			style="width: 50%"
			absolute
			temporary
		>
			<v-row no-gutters style="">
				<v-col>
					<v-list nav dense>
						<v-list-item-group
							v-model="group"
							active-class="deep-purple--text text--accent-4"
						>
							<v-list-item>
								<v-list-item-title>Foo</v-list-item-title>
							</v-list-item>

							<v-list-item>
								<v-list-item-title>Bar</v-list-item-title>
							</v-list-item>

							<v-list-item>
								<v-list-item-title>Fizz</v-list-item-title>
							</v-list-item>

							<v-list-item>
								<v-list-item-title>Buzz</v-list-item-title>
							</v-list-item>
						</v-list-item-group>
					</v-list>
				</v-col>
				<v-col> Hello </v-col>
			</v-row>
		</v-navigation-drawer>
	</div>
</template>

<script>
export default {
	data() {
		return {
			drawer: false,
			group: null,
		};
	},
	watch: {
		group() {
			this.drawer = false;
		},
	},
};
</script>