<script setup lang="ts">

defineProps<{
    title: string,
    body: string
    nomination: string
}>();

</script>

<template>
    <div class="container">
        <div class="award">{{ title }}</div>
        <div class="body">{{ body }}</div>
        <div class="nomination">номинация {{ nomination }}</div>
    </div>
</template>
<style scoped>
.container {
    display: flex;
    flex-direction: column;
    width: calc(25vw ) ;
}

.award {
    text-transform: uppercase;
}

.body {
    font-size: 1rem;
}

.nomination {
    font-size: 0.75rem;
    color: #FF6000;
}
</style>