<template>
    <div class="navBer">
        <div class="navBerLeft">
            <slot name='left'></slot>
        </div>
        <div class="navBerCenter">
            <slot name="center"></slot>
        </div>
        <div class="navBerRight">
            <slot name="right"></slot>
        </div>
    </div>
</template>

<script>
export default {
  name:"NavBer",
  components:{},
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

.navBer{
    height: 2.9333rem;
    display: flex;
    line-height: 2.9333rem;
    text-align: center;
}
.navBerLeft,.navBerRight{
    width: 5rem;
    flex: 1 0 none;
}
.navBerCenter{
    flex: 1;
}
</style>