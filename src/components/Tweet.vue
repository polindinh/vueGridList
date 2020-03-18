<template>
    <div>
        <h2>{{author}}</h2>
        <p>{{content}}</p>
    </div>
</template>

<script>
    export default {
    name: 'Tweet',
    props :{
        id:{
            type:Number,
            required:true,
        },
        content:{
            type:String,
            required:true,
        },
        author:{
            type:String,
            required:true,
        }
    },    
        
};
</script>

<style scoped>

</style>