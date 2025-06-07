<script lang="ts" setup>
defineProps<{
    image: string,
    barcode: string,
    name: string,
    descripion: string,
    caseNumber: string,
    tags: string[]
}>();
</script>

<template>
    <div class="wrapper">
        <div class="container">
            <div class="head">
                <div class="number">
                    <div class="head-left">
                        <div class="circle"></div>
                        case {{ caseNumber }}
                    </div>
                    <img :src="barcode" alt="">
                </div>
                <div class="text">{{ descripion }}</div>
                <div class="line bold"></div>
                <div class="line thin"></div>
                <h1>{{ name }}</h1>
            </div>
            <img :src="image" alt="" class="content">
        </div>
        <div class="tagsList">
            <div v-for="tag in tags" :key="tag" class="tagElement">{{ tag }}</div>
        </div>
    </div>
</template>

<style scoped>
h1 {
    font-size: 5rem;
}
.wrapper{
    margin-top: 50px;
    padding-bottom: 100px;
    border-bottom: 50px;
}
.content {
    justify-self: end;
    width: 100%;
}

.container {
    border-radius: 55px;
    border: 3px solid black
}

.head-left {
    display: flex;
    font-size: 2rem;
    align-items: center;
    gap: 10px;
    padding-left: 10px;
}

.head {
    margin: 25px;

}

.thin {
    margin-top: 5px;
    height: 3px;
}

.bold {
    margin-top: 10px;
    height: 9px;
}

.line {
    width: 100%;
    background-color: black;
}

.text {
    width: 80%;
}

.number {
    display: flex;
    justify-content: space-between;
    text-transform: uppercase;
}

.circle {
    height: 36px;
    width: 36px;
    border-radius: 50%;
    background-color: black;
}

.tagsList {
    margin-top: 20px;
    display: flex;
    gap: 15px;
    justify-content: start;
    align-items: start;
}

.tagElement {
    text-transform: uppercase;
    padding: 15px;
    border: 1px solid black;
    border-radius: 15px;
    
}
</style>