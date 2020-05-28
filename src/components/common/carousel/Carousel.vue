

<template>
  <div class="carousel">
    <el-carousel indicator-position="outside" :autoplay='autoplay'>
      <el-carousel-item v-for="item in bannerImgList" :key="item.acm">
        <a :href="item.link" class="bannerLink">
          <img :src="item.image" alt class="bannerImg" />
        </a>
      </el-carousel-item>
    </el-carousel>
  </div>
</template>



<script>
export default {
  name: "Carousel",
  components: {},
  props: {
    imgList: {
      type: Array,
      default() {
        return []
      }
    }
  },
  data() {
    return {
      autoplay:true
    };
  },
  watch: {},
  computed: {
    bannerImgList() {
      return this.imgList;
      console.log(this.imgList);
    }
  },
  methods: {},
  created() {},
  mounted() {}
};
</script>
<style>
.carousel {
  width: 100%;
  height: 10rem;
  margin-bottom: 1.8667rem;
}
 .el-carousel__item{
   height:10rem;
   
 }

 .el-carousel__item .bannerImg{
  width: 100%;
  height: auto;
 }

 .el-carousel__container{
   height: 10rem;
 }
 .bannerLink{
   display:block;
   width: auto;
   height: 10rem;
   
 }
 

</style>