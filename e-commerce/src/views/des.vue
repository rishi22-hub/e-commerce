<template>
  <div class="des">
   
   
   <img :src="itemm.image" style="width:200px; height:200px;" alt="fkndjfn">
   <br>
{{itemm.title}}
<br>
 ${{itemm.price}} 

    {{itemm.description}} 
 
   
    
  </div>
</template>

 <script>

import axios from 'axios'
// import useRoute from 'vue-router';
 export default{
   name:'des',
   data(){
    return{

      idd:this.$route.params.id,
     
      itemm:{}
    }
  },
  components:{

  },
  mounted(){
    //   const route=useRoute();
      
     
    
   axios.get("https://fakestoreapi.com/products/"+this.idd)
    .then((result) =>{
      this.itemm=result.data;
    }).catch(() => {
    console.warn('Not good man :(');
    
});
  }
 }
</script>