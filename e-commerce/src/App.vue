<template>
 <div id="nav">

<ul>
  <li><img src="https://th.bing.com/th/id/OIP.XiJaMWJmd7llMMmf-3vOYAHaHa?pid=ImgDet&rs=1"  style="width:100px; height:80px;"></li>
  <router-link to="/home"> <li><a>Home</a></li></router-link>
   <router-link to="/men"> <li><a>Mens</a></li></router-link>
    <router-link to="/women"> <li><a>women</a></li></router-link>
     <router-link to="/jewelry"> <li><a>jewelry</a></li></router-link>
      <router-link to="/electronics"> <li><a>electronic</a></li></router-link>
<h1 id="h11"><li>FLIPKART</li></h1>
 <router-link to="/contact"> <li class="cc"><a>Contact</a></li></router-link>
 <router-link to="/about"> <li class="cc"><a>About</a></li></router-link>
  <router-link to="/about"> <li class="cc"><a>login</a></li></router-link>
</ul>

 

 
  <router-view/>
   <hr>
<Foot/>
 </div>
</template>

<script>
import Foot from "@/views/end.vue";
export default {
  name: "nav",
  components: {
    Foot,
  }
};
</script>



<style>

#h11{
  color:yellow;
  margin-left: 25%;
  padding-left: 20%;
}
button{
  color:red;
  margin-left: 1100%;
  padding-left: 10%;
}
ul {
  list-style-type: none;
  margin: 0;
  padding: 0;
  overflow: hidden;
  background-color:skyblue;
}

li {
  float: left;
  margin-top: 1%;
}

li a {
  display: block;
  color: white;
  text-align: center;
  padding: 14px 16px;
  text-decoration: none;
}

/* Change the link color to #111 (black) on hover */
li a:hover {
  background-color:skyblue;
}
ul {
  list-style-type: none;
  margin: 0;
  padding: 0;
}
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
.cc{
  margin-left:3%;
  margin-right: 0%;
  margin-top: 0%;

}

</style>