<template>
    <h1>{{ title }}</h1>
    <ButtonOne outlined @click="increments">Click me!</ButtonOne>
    <DirectivesTest />
</template>

<script>
import ButtonOne from './components/ButtonOne.vue';
import DirectivesTest from './components/DirectivesTest.vue';

export default {
    name: 'App',
    components: {
        ButtonOne,
        DirectivesTest,
    },
    data() {
        return {
            amountOfClick: 0,
        };
    },
    computed: {
        title() {
            return `Amount of click ${this.amountOfClick}`;
        },
    },
    methods: {
        increments() {
            this.amountOfClick += 1;
        },
    },
};
</script>

<style>
#app {
    font-family: Avenir, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
    margin-top: 60px;
}
</style>
