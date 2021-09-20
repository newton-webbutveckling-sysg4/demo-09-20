<template>
	<div class="selector">
		<h2> Select a bird </h2>

		<button v-on:click="sendInfo(ravenFact)"> Raven </button>
		<button v-on:click="sendInfo(ostrichFact)"> Ostrich </button>
	</div>
</template>

<script>
// sendInfo(ravenFact)
// sendRavenInfo
export default {
	data: () => ({
		ravenFact: 'A raven can live for 10-15 years. Wingspan of 100-150 cm. Oden had two ravens.',
		ostrichFact: 'An ostrich can run for 70 km/h. Ostriches can weigh up to 140 kg.'
	}),

	methods: {
		sendInfo(fact) {
			console.log('Emitting bird fact to parent');
			// emit ( namnet på funktionen, data som ska skickas )
			this.$emit('birdSelected', fact)
		}
	}
}
</script>

<style scoped>

</style>
