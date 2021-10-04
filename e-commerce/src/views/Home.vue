<template>
  <div class="Home">
   <div id="rrr" v-for="item in l" :key="item.id" border="1">
   
   <img :src="item.image" style="width:200px; height:200px;">
   <br>
{{item.title}}
<br>
${{item.price}}
<br>
<button id="tt">Add to Cart</button>
    </div>
    
   
    
  </div>
</template>

 <script>

import axios from 'axios'

 export default{
   name:'Home',
   data(){
    return{
      l:undefined
    }
  },
  components:{

  },
  mounted(){
   axios.get("https://fakestoreapi.com/products")
    .then((result) =>{
      this.l=result.data;
    }).catch(() => {
    console.warn('Not good man :(');
});
  }
 }
</script>
<!-- export default {
  
  name: 'home',
  data(){
    return{
      l:[]
    }
  },
  components:{

  },
  mounted(){
    Vue.axios.get("https://fakestoreapi.com/products")
    .get((result) =>{
      this.l=result;
    });
  }

}
-->
<style>
#tt{
  display: inline-block;
        background-color: #7b38d8;
        border-radius: 3px;
        border: 4px double #cccccc;
        color: #eeeeee;
        text-align: center;
        font-size: 20px;
        padding: 20px;
        width: 150px;
        -webkit-transition: all 0.5s;
        -moz-transition: all 0.5s;
        -o-transition: all 0.5s;
        transition: all 0.5s;
        cursor: pointer;
        margin: 5px;
}
</style>