<template>
    <div>
        <h1>Child comp</h1>
        <ul>
      <li v-for="(item,index) in arr" :key="index">{{item}} <button @click="Sil(index)">Delete</button></li>
     </ul>
    </div>
</template>

<script>
export default {
    data(){
        return{
         
        }
    },
    methods:{
      Sil(index){
    this.arr.splice(index,1)
      }
    },
    props:["arr"]
}
</script>