<template>
    <h1>Hello world</h1>
    <button @click="start" :disabled="isPlaying">play</button>
    <Block v-if="isPlaying" :delay="delay" @end="endGame" />
    <Results v-if="showResults" :score="score" />
</template>

<script>

import Block from './components/Block.vue';
import Results from './components/Results.vue';



export default {
  name: 'App',
  data(){
    return {
        isPlaying: false,
        delay: null,
        score: null,
        showResults: false
    }
  },
  components: {
    Block,
    Results
  },
  methods: {
    start(){
        this.delay = 2000 + Math.random() * 5000
        this.isPlaying = true 
        this.showResults = false
    },

    endGame(reactionTime){
        this.score = reactionTime;
        this.isPlaying = false
        this.showResults = true 
    }



  }
  
}
</script>

<style>
#app {
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
h1{
    font-size: 30px;
    color: rgb(16, 88, 88);
}
button{
    padding: 5px 20px;
    background: rgb(16, 88, 88);
    color: white;
    border-radius: 5px;
    cursor: pointer;
    border: none;
}
button[disabled]{
    cursor: not-allowed;
    opacity: 0.2;
}
</style>
