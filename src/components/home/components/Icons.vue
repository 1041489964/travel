<template>
  <div class="iconsBox">
    <swiper  :options="swiperOption">
      <!-- slides -->
      <swiper-slide v-for="(page,index) in pages" :key="index">
        <div class="icons">
          <div class="icon" v-for="(item,index) in page" :key="index">
            <div>
              <img :src="item.imgUrl" alt="">
            </div>
            <p>{{item.desc}}</p>
          </div>
        </div>
      </swiper-slide>
      <!-- Optional controls -->
<!--
      <div class="swiper-pagination" slot="pagination"></div>
-->

    </swiper>
  </div>
</template>
<script>

  export default {
    name: 'HomeIcon',
    data() {
      return {
        swiperOption: {
          pagination: '.swiper-pagination',
          loop:false
        },
        iconsData: [
          {
            imgUrl: "http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png",
            desc: '景点门票'
          },
          {
            imgUrl: "http://img1.qunarzz.com/piao/fusion/1804/ff/fdf170ee89594b02.png",
            desc: '必游榜单'
          },
          {
            imgUrl: "http://img1.qunarzz.com/piao/fusion/1803/6a/45f595250c73d102.png",
            desc: '夏日玩水'
          },
          {
            imgUrl: "http://img1.qunarzz.com/piao/fusion/1803/47/c2b659e048b11602.png",
            desc: '主题乐园'
          },
          {
            imgUrl: "http://img1.qunarzz.com/piao/fusion/1803/76/eb88861d78fb9902.png",
            desc: '动植物园'
          },
          {
            imgUrl: "http://img1.qunarzz.com/piao/fusion/1803/6c/9e54a8540fee0102.png",
            desc: '故宫'
          },
          {
            imgUrl: "http://img1.qunarzz.com/piao/fusion/1804/5a/13ceb38dcf262f02.png",
            desc: '一日游'
          },
          {
            imgUrl: "http://img1.qunarzz.com/piao/fusion/1803/54/35899492b1302802.png",
            desc: '乐园'
          },
          {
            imgUrl: "http://img1.qunarzz.com/piao/fusion/1803/95/8246f27355943202.png",
            desc: '游乐场'
          },
          {
            imgUrl: "http://img1.qunarzz.com/piao/fusion/1803/80/416c6ab3368d1f02.png",
            desc: '全部玩乐'
          },
        ]
      }
    },
    methods: {},
    computed: {
      pages() {
        const pages = [];
        this.iconsData.forEach((item,index)=>{
          const page = Math.floor(index/8);
          if(!pages[page]){
            pages[page]=[]
          }
          pages[page].push(item)
        });
        return pages;
      }
    },
    components: {}
  }
</script>
<style lang="less" scoped>
  @import (reference) "~style/common.less";

  .icons {
    display: flex;
    flex-wrap: wrap;

    overflow: hidden;
    height: 0;
    padding-bottom: 50%;

    .icon {
      width: 25%;
      text-align: center;

      div {
        width: 1.1rem;
        height: 1.1rem;
        margin: 0 auto;
        padding-top: .1rem;
        img {
          display: block;
          width: 100%;
        }
      }

      p {
        margin-top: .1rem;
        color: #212121;
        font-size: .28rem;
        .ellipsis;
      }
    }

  }
</style>
