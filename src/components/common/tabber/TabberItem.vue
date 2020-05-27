<template>
    <div class="tabberItem" @click="tabberItemClick" :class={active:isActive}>
        <slot name='iconFont'></slot>
        <slot name="iconTxt"></slot>
    </div>
</template>

<script>
export default {
  name:"TabberItem",
  components:{},
  props:{
      path:String
  },
  data(){
    return {
    }
  },
  watch:{},
  computed:{
      isActive (){
          return this.$route.path.indexOf(this.path) != -1
      }
  },
  methods:{
      tabberItemClick (){
         if(this.$route.path != this.path){
             this.$router.push(this.path)
             console.log(this.$route.path,this.path);
             
         }
        
         
      }
  },
  created(){
      
  },
  mounted(){}
}
</script>
<style>
    
</style>