<template>
    <div id="tab-bar">
        <slot></slot>
    </div>
</template>

<script>
    import TabBarItem from "./TabBarItem";
    export default {
        name: "TabBar",
        components: {TabBarItem}
    }
</script>

<style scoped>
    #tab-bar {
        display: flex;
        background-color: #f6f6f6;

        position: fixed;
        right: 0;
        left: 0;
        bottom: 0;

        box-shadow: 0 -1px 0 #888888;
    }
</style>
