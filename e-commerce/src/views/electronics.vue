<template>
  <div class="electronics">
      <h1>fndnjcn</h1>
   <div id="rrr" v-for="item in ll" :key="item.id" border="1">
   
   <img :src="item.image" style="width:200px; height:200px;">
   <br>
{{item.title}}
<br>
${{item.price}}
<br>
<p><button>Add to Cart</button></p>
    </div>
    
   
    
  </div>
</template>

 <script>

import axios from 'axios'

 export default{
   name:'electronics',
   data(){
    return{
      ll:undefined
    }
  },
  components:{

  },
  mounted(){
   axios.get("https://fakestoreapi.com/products/category/electronics")
    .then((result) =>{
      this.ll=result.data;
    }).catch(() => {
    console.warn('Not good man :(');
});
  }
 }
</script>