<template>
    <div>
        <button @click="() => $root.$emit(`toast_notify`, `Successfully Posted!`)">POST</button>
    </div>
</template>

<script>
    export default {
    }
</script>

<style scoped>

</style>