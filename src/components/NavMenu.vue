<template>
    <nav>
        <div class="navMenu">
            <ul>
                <li class="navItem"><a href="">Features</a></li>
                <li class="navItem"><a href="">Pricing</a></li>
                <li class="navItem"><a href="">Resources</a></li>
            </ul>
            <div class="lineDivider"></div>
            <ul>
                <li class="navItem"><a href="">Login</a></li>
                <li>
                    <ButtonComponent 
                        :text="'Sign Up'"
                        :fullWidth="true"
                    />
                </li>
            </ul>
        </div>
    </nav>
</template>
<script>
import ButtonComponent from './common/ButtonComponent.vue';
export default {
    name: 'NavMenu',
    components: {
        ButtonComponent,
    }
}
</script>
<style scoped>
nav {
    @apply
        absolute
        top-24
        px-6
        w-full
}

.navMenu {
    @apply
        flex
        flex-col
        gap-8
        bg-Dark-Violet
        text-center
        rounded-lg
        px-6
        py-10
        w-full
        h-full
}
.navMenu > ul {
    @apply
        flex
        flex-col
        gap-8
}
.navItem {
    @apply
        text-white
        font-bold
        text-lg
}
.lineDivider {
    @apply
        w-full
        border-t-2
        border-Gray
        opacity-20
        
}
</style>