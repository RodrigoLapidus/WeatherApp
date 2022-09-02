<script setup>
import { createDOMCompilerError } from '@vue/compiler-dom';
import HelloWorld from './components/HelloWorld.vue';
  
const APIkey = "fdd16dabda152dda4648159c6ca7973f";

const city = "Detroid";

created() {
  this.getCurrentWeather();
}

getCurrentWeather() {
    fetch(`https://api.openweathermap.org/data/2.5/weather?q=${this.city}&appid=${this.APIkey}`)
    
    // check if the data is showing
    .then((res) =>
      console.log(res.data);
    )};

</script>

<template>
  <div>
    
  </div>
</template>

<style>
  body {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: 'Quicksand', sans-serif;
  }
</style>
