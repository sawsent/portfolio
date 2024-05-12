<script setup>
import ExperienceComponent from './ExperienceComponent.vue';
</script>

<template>
	<div id="experience">
		<ExperienceComponent 
			:iconSrc="endesa.iconSrc"
			:date="endesa.date"
			:title="endesa.title"
			:employer="endesa.employer"
			:description="endesa.description"
		/>
	</div>
</template>

<script>

export default {
	name: 'MainComponent',
	components: {
		ExperienceComponent
	},
	data() {
		return {
			endesa: {
				iconSrc: 'src/assets/CV/experience/test.png',
				date: 'Jan 2020 - Present',
				title: 'Lead Developer',
				employer: 'Creative Solutions',
				description: 'Leading a team of developers in creating innovative software solutions.'
			}
		};
	}
};
</script>

<style scoped>
#experience {
	display: flex;
	flex-direction: column;
}
</style>