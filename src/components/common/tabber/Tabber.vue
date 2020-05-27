<template>
    <div class="tabber">
        <ul>
            <!-- <router-link to='/home' tag='li'>首页</router-link>
            <router-link to='/category' tag='li'>分类</router-link>
            <router-link to='/cart' tag='li'>购物车</router-link>
            <router-link to='/profile' tag='li'>我</router-link> -->
            <tabber-item path='/home'>
                <span class="iconfont icon-shouye" slot='iconFont'></span>
                <span class="" slot='iconTxt'>首页</span>
            </tabber-item>
            <tabber-item path='/category'>
                <span class="iconfont icon-faxian" slot='iconFont'></span>
                <span class="" slot='iconTxt'>分类</span>
            </tabber-item>
            <tabber-item path='/cart'>
                <span class="iconfont icon-aixin" slot='iconFont'></span>
                <span class="" slot='iconTxt'>购物车</span>
            </tabber-item>
            <tabber-item path='/profile'>
                <span class="iconfont icon-wode" slot='iconFont'></span>
                <span class="" slot='iconTxt'>我</span>
            </tabber-item>
        </ul>
    </div>
</template>

<script>
import TabberItem from './TabberItem'
export default {
  name:"Tabber",
  components:{
      TabberItem
  },
  props:{},
  data(){
    return {
        
    }
  },
  watch:{},
  computed:{},
  methods:{},
  created(){},
  mounted(){}
}
</script>
<style>

.tabber{
    width:100%;
    position: fixed;
    height: 3.9333rem;
    bottom: 0;
    left: 0;
    right: 0;
    background: #fcfcfc;
}

.tabber ul {
    display: block;
    width:100%;
    height: 100%;
    display: flex;
    justify-content: space-between;
}
.tabberItem{
        flex: 1;
        text-align: center;   
    }
.tabberItem span{
    display: block;
    width: 100%;
    font-size: 0.8rem;
    line-height: 1.5rem;
}
.tabberItem .iconfont{
    font-size: 1.8rem;
    line-height: 2.433rem;
}

.tabber .active {
    color: red;
}
</style>