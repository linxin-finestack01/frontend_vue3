<template>
    <div class="person">
        <h2>name: {{ name }}</h2>
        <h2>age: {{ age }}</h2>
        <button @click="changeName">change name</button>
        <button @click="changeAge">change age</button>
        <button @click="showTel">see the tel</button>
    </div>
</template>

<script lang="ts" setup>
    import { ref } from 'vue'

    let name = ref('zhangsan') // 非响应式
    let age = ref(18) // 非响应式
    let tel = '1388888888'

    function showTel() {
        alert(tel)
    }

    function changeName() {
        name.value = 'lisan' // 非响应式
    }

    function changeAge() {
        age.value += 1 // 非响应式
    }
</script>

<style scoped>
.person {
    background-color: skyblue;
    box-shadow: 0 0 10px;
    border-radius: 10px;
    padding: 20px;
}
button {
    margin: 5px;
}
</style>