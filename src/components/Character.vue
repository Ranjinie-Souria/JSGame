<template>
    <div class="character">
    <img style="position: relative;" src="../assets/base.png" alt="">
        <div v-if="ears === 1"><img  style="position: absolute;z-index:1;left:320px;top:750px;" src="../assets/1.png" alt=""></div>
        <div v-else-if="ears === 2"><img  style="position: absolute;z-index:1;left:320px;top:750px;" src="../assets/2.png" alt=""></div>
        <div v-else-if="ears === 3"><img  style="position: absolute;z-index:1;left:320px;top:750px;" src="../assets/3.png" alt=""></div>
        <div v-else-if="ears === 4"><img  style="position: absolute;z-index:1;left:320px;top:750px;" src="../assets/4.png" alt=""></div>
        <div v-if="hair === 1"><img  style="position: absolute;z-index:1;left:320px;top:750px;" src="../assets/h1.png" alt=""></div>
        <div v-else-if="hair === 2"><img  style="position: absolute;z-index:1;left:320px;top:750px;" src="../assets/h2.png" alt=""></div>
        <div v-else-if="hair === 3"><img  style="position: absolute;z-index:1;left:320px;top:750px;" src="../assets/h3.png" alt=""></div>
        <div v-else-if="hair === 4"><img  style="position: absolute;z-index:1;left:320px;top:750px;" src="../assets/h4.png" alt=""></div>
        <div v-if="eyes === 1"><img  style="position: absolute;z-index:1;left:320px;top:750px;" src="../assets/e1.png" alt=""></div>
        <div v-else-if="eyes === 2"><img  style="position: absolute;z-index:1;left:320px;top:750px;" src="../assets/e2.png" alt=""></div>
        <div v-else-if="eyes === 3"><img  style="position: absolute;z-index:1;left:320px;top:750px;" src="../assets/e3.png" alt=""></div>
        <div v-else-if="eyes === 4"><img  style="position: absolute;z-index:1;left:320px;top:750px;" src="../assets/e4.png" alt=""></div>
    </div>
</template>

<script>
    export default {
        name: 'Character',
        props: {
            name: String,
            ears: Number,
            hair: Number,
            eyes: Number
        },
        data: function () {
            return {

            }
        },
        mounted() {
        },
    methods: {

    }
    }
</script>

<style scoped>
</style>