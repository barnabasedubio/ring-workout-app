<template>
	<v-app dark>
		<v-navigation-drawer app fixed expand-on-hover permanent>
			<v-list>
				<v-list-item
					v-for="(item, i) in items"
					:key="i"
					:to="item.to"
					router
					exact
				>
					<v-list-item-action>
						<v-icon>{{ item.icon }}</v-icon>
					</v-list-item-action>

					<v-list-item-content>
						<v-list-item-title v-text="item.title" />
					</v-list-item-content>
				</v-list-item>
			</v-list>
		</v-navigation-drawer>

		<v-app-bar fixed app>
			<v-toolbar-title class="app-title" v-text="title" />
		</v-app-bar>

		<v-main>
			<v-container>
				<nuxt />
			</v-container>
		</v-main>

		<v-footer :absolute="!fixed" app>
			<span>&copy; {{ new Date().getFullYear() }} Barnabas Edubio</span>
		</v-footer>
	</v-app>
</template>

<script>
export default {
	data() {
		return {
			fixed: false,
			items: [
				{
					icon: "mdi-dumbbell",
					title: "Exercises",
					description: "",
					to: "/exercises",
				},
				{
					icon: "mdi-chart-line",
					title: "Stats",
					description: "",
					to: "/stats",
				},
				{
					icon: "mdi-calendar",
					title: "Plan",
					description: "",
					to: "/plan",
				},
				{
					icon: "mdi-account-multiple",
					title: "Friends",
					description: "",
					to: "/friends",
				},
			],
			miniVariant: false,
			right: true,
			rightDrawer: false,
			title: "RingHub",
		}
	},
}
</script>

<style lang="scss">
* {
	box-sizing: border-box;
}
.app-title {
	margin: 0 auto;
}
</style>
