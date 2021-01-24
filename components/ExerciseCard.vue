<template>
	<v-col cols="12" xl="4" lg="4" sm="6" xs="12">
		<v-card class="exercise-card">
			<v-card-title> Dips </v-card-title>
			<youtube
				class="youtube-player"
				:host="videoHost"
				:video-id="videoId"
				:player-width="playerWidth"
				:mute="startMuted"
			></youtube>
		</v-card>
	</v-col>
</template>

<script>
export default {
	data() {
		return {
			videoId: "KxT0MMlH1lY",
			videoHost: "https://www.youtube-nocookie.com",
			playerWidth: "100%",
			startMuted: true
		};
	},
};
</script>

<style lang="scss" scoped>
</style>
