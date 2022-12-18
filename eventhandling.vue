<template>
  <h2>{{name}}</h2>
<div>
  <button v-on:click="name = 'batman'">change name</button>
  <button v-on:mouseover="name = 'batman'">change name</button>
</div>

<h2>{{count}}</h2>
<div>
  <button v-on:click="increment(1)">Increment1</button>
  <button v-on:click="decrement(1)">Decrement1</button>
  <button v-on:click="increment(5)">Increment5</button>
  <button v-on:click="decrement(5)">Decrement5</button>
</div>

</template>

<script>
export default {
  name: 'App',
  data(){
    return {     
     name: 'vishwas',
     count : 0
    }
  },
  methods : {
    increment(num) {
      this.count +=num
    },
    decrement(num) {
      this.count-=num
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
