
<script setup>

import ChildVue from './components/Child.vue';

</script>
<template>
  <div>    
<h1>App comp</h1>
    <input type="text" v-model="inp_val">
     <button @click="Send">Gonder</button>


     <hr>

    

      <ChildVue :arr="arr"  />

  </div>
</template>
<script>
export default {
  data(){
    return{
      inp_val:"",
      arr:[],
      


    }
  },
  methods:{
    Send(){
      this.arr.push(this.inp_val)
      this.inp_val=""
    
    }
  }
}
</script>