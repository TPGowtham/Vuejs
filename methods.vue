<template>
<h2>Add method = {{ add(2,4,5) }}</h2>
<h2>Add method = {{ add(32,44,55) }}</h2>
<h2>Multiply method = {{ multiply(2) }}</h2>
</template>

<script>
export default {
  name: 'App',
  data(){
    return {     
      baseMultiplier: 5 
    }
  },
  methods : {
    add(a,b,c) {
      return a+b+c;
    },
    multiply(num) {
      return num * this.baseMultiplier
    }
  },
  
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
