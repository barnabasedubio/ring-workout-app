<template>
	<v-row>
		<v-col cols="12" xl="12">
			<v-card>
				<v-card-title>
					<h1>Vertical Push</h1>
				</v-card-title>
			</v-card>
		</v-col>
		<exercise-card></exercise-card>
	</v-row>
</template>

<script>
import ExerciseCard from "~/components/ExerciseCard";
export default {
	head() {
		return {
			title: "Exercises",
		};
	},
	components: {
		ExerciseCard,
	},
};
</script>

<style scoped lang="scss"></style>
