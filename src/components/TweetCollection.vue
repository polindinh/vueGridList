<template>
    <div id="tweets" v-bind:style='{"display" : (isActive? "grid" : "block" )}'>
        <Tweet v-for="tweet in TweetCollection" :key="tweet.id" :id="tweet.id" :author="tweet.author" :content="tweet.content"/>
    </div>
</template>

<script>
    import Tweet from './Tweet.vue'
    export default {
        name: 'TweetCollection',
        props:{
            TweetCollection: Array,
        },
        components: {
            Tweet,
        
        },
        data() {
            return {
                isActive: true
            };
        },
        mounted: function(){
            this.$root.$on('changeToList', this.changeToList)
        },
        methods:{
            changeToList: function(){
                this.isActive = !this.isActive;

            }
        },
};
</script>

<style scoped>

</style>