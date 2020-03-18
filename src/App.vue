<template>
  <div id="app">
    <Button/>
    <TweetCollection v-bind:TweetCollection="tweets"/>
  </div>
</template>

<script>
import Button from './components/Button.vue'
import TweetCollection from './components/TweetCollection.vue'


export default {
  name: 'App',
  components: {
    Button,
    TweetCollection,
  },
  data(){
    return{
      tweets:[
        {id: 1, content: 'See You Again', author: 'Charlie Puth'},
        {id: 2, content: 'Apologize', author: 'OneRepbulic'},
        {id: 3, content: 'Fix You', author: 'Coldplay'},
        {id: 4, content: 'Intentions', author: 'Justin Bieber'},
        {id: 5, content: 'My heart will go on', author: 'Celine Dion'},
        {id: 6, content: 'Pressure', author: 'Queen'},
      ],
    }
  },
}
</script>

<style>
body{
    margin: 0;
    font-family: 'Nunito SemiBold';
}

#tweets{
   display:grid;
   grid-template-columns: 1fr 1fr 1fr;
   justify-items: center;
   text-align: center;
}

h1, p{
    text-align: center;
}
#toggle-button{
  margin-top:20px;
  display: flex;
  align-items: center;
  justify-content: center;}
button{
  text-align: center;
  padding: 5px 10px;
  background-color: blue;
  color: white;
  font-size: 1.5em;
}
</style>
