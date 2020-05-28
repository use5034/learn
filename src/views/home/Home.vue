<template>
  <div class="home">
   <NavBer class="homeNavber">
     <span slot="center">购物街</span>
   </NavBer>
   <Carousel :imgList='bannerList'>
    
   </Carousel>
  </div>
</template>



<script>
// @ is an alias to /src

import NavBer from '@/components/common/navBer/NavBer.vue'
import {getHomeMultiData ,test} from '@/netwrok/home'
import Carousel from '@/components/common/carousel/Carousel'
export default {
  name: 'Home',
  data (){
    return {
      bannerList : []
    }
  },
  components: {
   NavBer,
   Carousel
  },
  created (){
    getHomeMultiData().then(res => {
      
      this.bannerList = res.data.banner.list;
      console.log(this.bannerList);
      
    })

   
  }
}
</script>

<style >
.homeNavber {
  background :pink;
  color: white;

}
</style>