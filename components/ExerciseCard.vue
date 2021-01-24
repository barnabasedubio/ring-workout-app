<template>
	<v-col cols="12" xl="4" lg="4" sm="6" xs="12">
		<v-card class="exercise-card">
			<v-card-title>{{ exerciseTitle }}</v-card-title>
			<client-only>
				<youtube
					class="youtube-player"
					:video-id="videoId"
					:player-width="playerWidth"
					:mute="startMuted"
				></youtube>
			</client-only>
		</v-card>
	</v-col>
</template>

<script>
export default {
	data() {
		return {
			videoId: "KxT0MMlH1lY",
			playerWidth: "100%",
			startMuted: true,
		};
	},
	computed: {
		exerciseTitle() {
			return this.$store.state.exercises.exerciseTitle;
		},
	},
};
</script>

<style lang="scss" scoped></style>
