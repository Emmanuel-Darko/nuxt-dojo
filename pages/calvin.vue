<template>
    <div>
        <p>Calvin </p>
        <p>{{ active }}</p>
        <p><button @click="setActive" class="is-border" :class="{isActive: active}" :style="{padding: padding}">{{status}}</button></p>
    </div>
</template>

<script setup>
    // states /data
    const active = ref(false)
    const padding = ref('0')
    const status = ref('mia me')
    // methods
    const setActive = () => {
        active.value = !active.value
        status.value = status.value == 'mia me' ? 'gyae me' : 'mia me'
        changePadding()
    }
    const changePadding = () => {
        padding.value = padding.value == '0' ? '20px' : '0'
    }

    definePageMeta({
        layout: 'products'
    })
</script>

<style lang="css" scoped>
button{
    background-color: red;
}
button.isActive{
    background-color: greenyellow;
}
.is-border{
    border-radius: v-bind(padding);
}

</style>