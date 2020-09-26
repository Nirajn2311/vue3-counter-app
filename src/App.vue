<template>
    <h1>VUE3 COUNTER APP</h1>
    <div>
        <div id="counter">
            <h2>{{ counter }}</h2>
        </div>
        <div id="buttons">
            <button @click="inc">INCREMENT</button>
            <button @click="dec">DECREMENT</button>
            <button @click="reset">RESET</button>
        </div>
    </div>
</template>

<script>
import { ref } from "vue";

export default {
    name: "App",
    setup() {
        const counter = ref(0);
        function inc() {
            counter.value++;
        }
        function dec() {
            counter.value--;
        }
        function reset() {
            counter.value = 0;
        }
        return { counter, inc, dec, reset };
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

#counter {
    margin: 10px;
}

button {
    margin: 0px 10px;
}
</style>
