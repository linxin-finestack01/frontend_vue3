<template>
    <div class="person">
        <h2>name: {{ name }}</h2>
        <h2>age: {{ age }}</h2>
        <button @click="changeName">change name</button>
        <button @click="changeAge">change age</button>
        <button @click="showTel">see the tel</button>
    </div>
</template>

<script lang="ts">
    export default {
        name: 'Person',
        setup() {
            let name = 'zhangsan' // 非响应式
            let age = 18 // 非响应式
            let tel = '1388888888'

            function showTel() {
                alert(tel)
            }

            function changeName() {
                name = 'lisan' // 非响应式
            }

            function changeAge() {
                age += 1 // 非响应式
            }

            return {
                name,
                age,
                tel,
                showTel,
                changeName,
                changeAge
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
button {
    margin: 5px;
}
</style>