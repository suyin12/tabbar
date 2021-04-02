<template>
    <div class="tab-bar-item" @click="itemClick">
        <div v-if="!isActive"><slot name="item-icon"></slot></div>
        <div v-else><slot name="item-icon-active"></slot></div>
        <slot name="item-text"></slot>
    </div>
</template>

<script>
    export default {
        name: "TabBarItem",
        props:{
            path: String
        },
        methods: {
            itemClick() {
                this.$router.replace(this.path)
            }
        },
        computed: {
            isActive() {
                return this.$route.path.indexOf(this.path) !== -1
            }
        }
    }
</script>

<style scoped>
    .tab-bar-item {
        flex: 1;
        text-align: center;
        height: 49px;
        margin-top: 3px;
        font-size: 14px;
        margin-bottom: 1px;
    }

    .tab-bar-item img {
        width: 29px;
        height: 29px;
        vertical-align: middle;
    }
</style>
