<template>
  <div>
    <nav-bar class="home-nav"><div slot="center">购物车</div></nav-bar>
    <!-- <h2>Home1</h2> -->
  </div>
</template>
<script>
import NavBar from "components/common/navbar/NavBar";
import {getHomeMultidata} from "network/home";
export default {
  name: "Home",
  components:{
    NavBar
  },
  created(){
    //1请求多个数据
    getHomeMultidata().then(res=>{
      console.log(res);
    })
  }
};
</script>
<style>
.home-nav{
  background-color: var(--color-tint);
  color:white;
}
</style>
