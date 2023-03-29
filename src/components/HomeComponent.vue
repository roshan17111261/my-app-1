<template>
   <div>
     <h1>{{ title }} component</h1>
     <button v-bind:disabled="disableBtn" @click="onclick">click me</button>
      <Users/>
      <Product/>
   </div>
</template>

<script>
import Users from './Users.vue';
import Product from './Product.vue'
export default{
    name:'HomeComponent',
    data(){
        return{
            title:'home',
            disableBtn: false
        }
       
    },
    components:{
        Users,
        Product
    },
    methods:{
        onclick(){
            this.title="roshan";
        }
    }
}
</script>
<style scoped>
div{
    background-color: aqua;
    height: 600px;
    align-items: center;
    text-align: center;
}
</style>
