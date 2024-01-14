<template>
    <div class="topBar">
        <div class="logo">Shortly</div>
        <button @click="handleClickNavButton" class="navButton">
            <font-awesome-icon :icon="['fas', 'bars']" />
        </button>
    </div>
</template>
<script>
export default {
    name: 'TopBar',
    methods: {
        handleClickNavButton(){
            this.$emit('onClickNavButton')
        }
    }
}
</script>
<style scoped>
.topBar {
    @apply  
        flex
        px-6
        pt-9
}
.logo {
    @apply
        font-bold
        text-3xl
        text-Very-Dark-Blue
}
.navButton {
    @apply
        text-2xl
        text-Grayish-Violet
        ml-auto
}
</style>