<template>
    <div v-for="(el, i) in friends" :key="i" class="">
        <p>This is Child Component by {{ el }}</p>
    </div>
</template>

<script>
export default {
    inject: ['friends']
}
</script>

<style scoped>
    div {
        background-color: aqua;
        padding: 1rem;
        width: 10rem;
        margin: auto;
    }
</style>