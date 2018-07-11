<template>
  <div class="wrapper">
    <swiper :options="swiperOption">
      <!-- slides -->
      <swiper-slide v-for="(item,index) in swiperList" :key="index">
        <img class="swiper-img"
             :src="item.imgUrl" alt="">
      </swiper-slide>

      <!-- Optional controls -->
      <div class="swiper-pagination" slot="pagination"></div>
    </swiper>
  </div>
</template>

<script>

  export default {
    name: "HomeSwiper",
    data() {
      return {
        swiperOption: {
          pagination: '.swiper-pagination',
          loop:true
        },
        swiperList:[{
            id:1,
            imgUrl:"http://img1.qunarzz.com/piao/fusion/1806/f5/ea83238744f31102.jpg_750x200_73b8477c.jpg"
          },
          {
            id:2,
            imgUrl:"http://img1.qunarzz.com/piao/fusion/1807/66/e5a5cec881702f02.jpg_750x200_67bb5691.jpg"
          },
          {
            id:3,
            imgUrl:"http://img1.qunarzz.com/piao/fusion/1806/3c/c72a1ccd4d7b2202.jpg_750x200_b88bbab4.jpg"
          },
          {
            id:4,
            imgUrl:"http://img1.qunarzz.com/piao/fusion/1803/5c/969bfa7af00a2702.jpg_750x200_b99b8e07.jpg"
          },
          {
            id:5,
            imgUrl:"http://img1.qunarzz.com/piao/fusion/1806/1c/4847ea66072c7b02.jpg_750x200_c32457fb.jpg"
          },
          {
            id:6,
            imgUrl:"http://img1.qunarzz.com/piao/fusion/1707/90/2ab6fd356529aa02.jpg_750x200_4120afc5.jpg"
          }]
      };
    }
  };
</script>

<style lang='less'>




  .wrapper {
    overflow: hidden;
    width: 100%;
    height: 0;
    padding-bottom: 26.57%;

    .swiper-pagination-bullet-active{
      background: #fff !important;
    }

    .swiper-img {
      width: 100%;
    }
  }
</style>
