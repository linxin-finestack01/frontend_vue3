<template>
    <div class="app">
        <h2>hello</h2>
        <Person />
    </div>
</template>

<script lang="ts">
    import Person from './component/Person.vue';
    export default {
        name: "App",
        components: { Person }
    }
</script>

<style>
.app {
    background-color: grey;
    box-shadow: 0 0 10px;
    border-radius: 10px;
    padding: 20px;
}
</style>