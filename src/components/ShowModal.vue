<template>
    <div class="custom-modal">
        <button class="show-modal" @click="toggle">Show modal</button>
        <modal v-if="visible" @close="toggle"></modal>
    </div>
</template>

<script>
    import Modal from './Modal';

    export default {
        components: {
            Modal,
        },

        data() {
            return {
                visible: false,
            }
        },

        methods: {
            toggle() {
                this.visible = !this.visible;
            }
        }
    }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
    .modal {

    }
</style>

