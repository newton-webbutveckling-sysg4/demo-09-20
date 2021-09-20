<template>
    <div class="">
        <h1> Demo using props and emit </h1>
        <BirdSelector v-on:birdSelected="selected"></BirdSelector>
        <BirdFact
            v-bind:fact="newFact"
            v-on:clearFacts="clear"></BirdFact>
    </div>
</template>

<script>
import BirdSelector from './components/BirdSelector'
import BirdFact from './components/BirdFact'

export default {
    name: 'App',
    components: {
        BirdSelector,
        BirdFact
    },

    data: () => ({
        newFact: ''
    }),
    methods: {
        selected(fact) {
            console.log('When a bird has been selected');
            this.newFact = fact
        },
        clear() {
            this.newFact = ''
        }
    }
}
</script>

<style>
.selector, .facts {
    border: 1px solid gray;
    padding: 1.5em;
    margin: 2em;
    border-radius: 2em;
}
#app {
    font-family: Avenir, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
    margin-top: 60px;
}
</style>
