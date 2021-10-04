<template>
  <div class="mens">
      <h1>fndnjcn</h1>
   <div id="rrr" v-for="item in ll" :key="item.id" border="1">
   
   <img :src="item.image" style="width:200px; height:200px;">
   <br>
<!-- <a href="https://fakestoreapi.com/products/"+"item.id"> -->
{{item.id}}
<br>
<router-link :to="'/des/' + item.id">{{item.title}}</router-link>

<!-- </a> -->
 
<br>
${{item.price}}
<br>
<button>Add to Cart</button>
    </div>
    
   
    
  </div>
</template>

 <script>

import axios from 'axios';

 export default{
   name:'mens',
   data(){
    return{
      ll:undefined
    }
  },
  components:{

  },
  mounted(){
   axios.get("https://fakestoreapi.com/products/category/men's%20clothing")
    .then((result) =>{
      this.ll=result.data;
    }).catch(() => {
    console.warn('Not good man :(');
   
});
  }
 }
</script>
<style>
button {
 margin-left:0%;
  display: inline-block;
  padding: 15px 25px;
  font-size: 20px;
  cursor: pointer;
  text-align: center;
  text-decoration: none;
  outline: none;
  color: #fff;
  background-color: #4CAF50;
  border: none;
  border-radius: 15px;
  box-shadow: 0 9px #999;
}

button:hover {background-color: #3e8e41}

button:active {
  background-color: #3e8e41;
  box-shadow: 0 5px #666;
  transform: translateY(4px);
}
</style>