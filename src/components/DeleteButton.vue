<template>
    <div>
        <button @click="handle_delete_click">DELETE</button>
    </div>
</template>

<script>
    export default {
        methods: {
            handle_delete_click: function() {
                this.$root.$emit(`toast_notify`, `Successfully Deleted!`);
            }
        }
    }
</script>

<style scoped>

</style>