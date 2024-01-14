<template>
    <button :class="[`rounded-${rounded}`, {'w-full': fullWidth }]">
        {{ text }}
    </button>
</template>
<script>
export default {
    name: 'ButtonComponent',
    props: {
        text: {
            type: String,
            required: true
        },
        rounded: {
            type: String,
            default: 'full',
            validator(value){
                return ['full', 'lg'].includes(value)
            }
        },
        fullWidth: {
            type: Boolean,
            default: false
        }
    }
}
</script>
<style scoped>
button {
    @apply
        bg-Cyan
        text-white
        font-bold
        text-lg
        py-3
        px-8
}
</style>