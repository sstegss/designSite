<script lang="ts" setup>
defineProps<{
    title: string,
    image: string,
    number: string
}>();
</script>


<template>
    <div class="container">
        <div class="body">
            <div class="number"> {{ number }}</div>

            <div class="title">{{ title }}</div>

        </div>
        <img :src="image" alt="">
    </div>
</template>


<style lang="css" scoped>
.body{
    display: flex;
}
.container {
    display: flex;
    justify-content: space-between;

}

.number {
    font-size: 0.75rem;
}

.title {
    margin-top: 15px;
    display: inline-block;
    font-size: 3rem;
    line-height: 2rem;
    text-transform: uppercase;

}
</style>