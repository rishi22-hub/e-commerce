<template>
  <div id="nav">
  <span>  <img id= "io" src = "https://assets.entrepreneur.com/content/3x2/2000/20180511063849-flipkart-logo-detail-icon.jpeg">
   <h1 id="ii">FLIPKART</h1></span>
    <span id="r">
    <router-link to="/">Home</router-link> |
    <router-link to="/about">About</router-link>
    </span>
   
    <hr>
    <Slider />
  </div>
  <router-view/>
</template>

<script>
import Slider from '@/components/HelloWorld.vue';
export default {
  name: "nav",
  components: {
    Slider
  }
};
</script>



<style>
#ii{
 text-align: center;
}
#nav {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  
  color: #2c3e50;
}
body {
  margin: 0px;
}
#io{
  
  height:70px;
  width:10%;
  align-items:left;
  padding-bottom: 0%;
}
#r{
  text-align-last: right;
  padding-bottom: 0%;
}
</style>