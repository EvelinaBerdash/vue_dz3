<template>
    <div class="costs-list">
        <slot name="head"></slot>
        <div v-for="cost in list" v-bind:key="cost.id" class="costs-list__item">
            <span v-for="(item, idx) in cost" v-bind:key="idx">{{ item }}</span>
        </div>
        <slot name="footer"></slot>
    </div>
</template>

<script>
    export default {
        name: 'List',
        props: {
            list: Array
        }
    }
</script>

<style lang="scss">
    .costs-list {
        width: 600px;
        margin: 0 auto;
        display: flex;
        flex-direction: column;

        &__item {
            height: 60px;
            border-bottom: 1px solid #444;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
    }
</style>