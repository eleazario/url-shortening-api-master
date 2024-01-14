<template>
    <TopBar @onClickNavButton="onClickNavButton"/>
    <NavMenu v-if="navMenuOpen"/>
</template>

<script>
import TopBar from './components/TopBar.vue';
import NavMenu from './components/NavMenu.vue'
export default {
    name: 'App',
    components: {
        TopBar,
        NavMenu
    },
    data(){
        return {
            navMenuOpen: false
        }
    },
    methods: {
        onClickNavButton(){
            this.navMenuOpen = !this.navMenuOpen
        }
    }
}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Poppins:wght@500;700&display=swap');
#app {
    font-family: 'Poppins', sans-serif;
    @apply
        relative
}
</style>
