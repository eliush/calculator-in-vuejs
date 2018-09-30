<template>
  <div id="app">
    <calculator></calculator>    
  </div>
</template>

<script>
import calculator from './components/calculator.vue';

export default {
  name: 'app',
  components:{
    "calculator": calculator,
  
  },
  data () {
    return {
      
    }
  }
}
</script>

<style>
html, body{
  margin: 0;
  height: 100%;
  font-family: 'Helvetica Neue', Arial, sans-serif;
  color: #333;
}
</style>
