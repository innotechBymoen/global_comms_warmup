<template>
    <div>
        <div v-for="(toast_message,i) in toast_messages" :key="i">
            <h1 >{{ toast_message }}</h1>
            <button @click="() => toast_messages.splice(i,1)">Clear Notification</button>
        </div>
    </div>
</template>

<script>
    export default {
        data() {
            return {
                toast_messages: []
            }
        },
        methods: {
            handle_toast: function(message) {
                if(this.toast_messages.length >= 3) {
                    this.toast_messages.splice(0,1);
                }
                this.toast_messages.push(message);
            },
        },
        mounted () {
            this.$root.$on(`toast_notify`, this.handle_toast);
        },
    }
</script>

<style scoped>

</style>