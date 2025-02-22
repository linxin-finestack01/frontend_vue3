<template>
    <div class="person">
        <h2>name: {{ name }}</h2>
        <h2>age: {{ age }}</h2>
        <button @click="showTel">see the tel</button>
    </div>
</template>

<script lang="ts">
    export default {
        name: 'Person',
        data() {
            return {
                name: 'zhangsan',
                age: 18,
                tel: '138888888'
            }
        },
        methods: {
            showTel() {
                alert(this.tel)
            }
        }
    }

</script>

<style scoped>
.person {
    background-color: skyblue;
    box-shadow: 0 0 10px;
    border-radius: 10px;
    padding: 20px;
}
</style>