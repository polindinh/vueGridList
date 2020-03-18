<template>
    <div id="toggle-button">
        <button @click="toggleToList">Change View Style</button>
    </div>
</template>

<script>
    export default {
        methods:{
            toggleToList: function(){
                this.$root.$emit('changeToList')
            }
        },
    }
</script>

<style scoped>

</style>