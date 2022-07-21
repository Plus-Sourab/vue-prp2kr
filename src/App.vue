<template>
  <h2>Volume Tracker </h2>
  <h3>Current Volume - {{volume}}</h3>
  <button @click= "volume+=2"> Increase</button>
  <button @click= "volume-=2"> Decrease</button>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'App',
  data(){
    return{
      volume: 0
    }
  },
  watch: {
    volume(newValue, oldValue){
      if(newValue > oldValue && newValue===16){
        alert("listening to a high volume for a long time may damage your hearing ")
      }
    }
    
  } 
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
