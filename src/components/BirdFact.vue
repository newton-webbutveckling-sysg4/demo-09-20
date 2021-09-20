<template>
	<div class="facts">
		<h2> Facts about the selected bird </h2>
		<p> {{ fact }} </p>
		<button v-on:click="clearFacts"> Clear facts </button>
	</div>
</template>

<script>
export default {
	props: ['fact'],
	methods: {
		clearFacts() {
			this.$emit('clearFacts')  // behöver inte någon data
		}
	}
}
// : kolon
// ; semikolon

</script>

<style scoped>

</style>
