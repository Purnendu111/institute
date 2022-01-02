<template>
	<v-app>
		<div>
			<v-row no-gutters style="">
				<v-col>
					<navbar />
				</v-col>
			</v-row>
			<v-row no-gutters style="">
				<v-col>
					<v-main>
						<router-view />
					</v-main>
				</v-col>
			</v-row>
		</div>
	</v-app>
</template>

<script>
import Navbar from "./components/navHeader/navbar.vue";

export default {
	name: "App",
	components: {
		Navbar,
	},

	data: () => ({
		//
	}),
};
</script>
