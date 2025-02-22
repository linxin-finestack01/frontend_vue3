<template>
    <div class="person">
        <h2>一辆汽车: {{ car.brand }}车,价值{{ car.price }}万</h2>
        <button @click="changePrice">修改汽车价格</button>
        <hr>
        <h2>游戏列表: </h2>
        <ul>
            <li v-for="g in game" :key="g.id">{{ g.name }}</li>
        </ul>
        <button @click="changeFirstGame">修改第一个游戏的名字</button>
    </div>
</template>

<script lang="ts" setup>
    import { reactive } from 'vue'

    let car = reactive({
        brand: '奔驰',
        price: 100
    })

    let game = reactive([
        { id: 'sdfsdf01', name: 'game1' },
        { id: 'sdfsdf02', name: 'game2' },
        { id: 'sdfsdf03', name: 'game3' }
    ])

    function changePrice() {
        car.price += 10
    }

    function changeFirstGame() {
        game[0].name = 'game4'
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
li {
    font-size: medium;
}
</style>