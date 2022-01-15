<template>
    <div v-show="selected" class="">
        Selected are {{ selected }}
    </div>
    <ChildComp />
</template>

<script>
import ChildComp from './ChildComp.vue'
export default {
    props: ['selected'],
    components: {
        ChildComp
    }
}
</script>

<style scoped>

</style>