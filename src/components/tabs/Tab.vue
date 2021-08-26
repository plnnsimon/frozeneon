<template>
<div v-if="isActive">
<slot></slot>
</div>
</template>

<script>

export default {
    name: "Tab",
    props: ['name', 'selected'],
    data() {
        return {
            isActive: false
        }
    },
    mounted() {
        this.isActive = this.selected;
    }
}

</script>