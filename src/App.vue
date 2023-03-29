<template>
  <div id="app">
    <h1 v-if="show">Hello {{ name }}</h1> 
     <h1 v-else>conditional rendering</h1> 
      <button @click="onClick">toggle</button>
      
    <home-component />
   
  </div>
</template>

<script>
import HomeComponent from './components/HomeComponent.vue';

export default {
  name: 'App',
  components:{
     HomeComponent,
    

  },
  data(){
    return{
        show: true,
        name: 'roshan'
    }
  },
  methods:{
    onClick(){
      this.show=!this.show;
      
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
