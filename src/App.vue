<template>
  <div id="app">
    <router-view></router-view>
    <Tabber></Tabber>
    
  </div>
</template>

<style>
@import 'assets/css/base.css';
@import url('//at.alicdn.com/t/font_1833622_4akhoiscbj2.css');
</style>
<script>
import Tabber from '@/components/common/tabber/Tabber'
export default {
  name:'App',
  components:{
    Tabber
  }
}
</script>