<template>
        <div class="home">
            <div class="swiper-container">
            <div class="swiper-wrapper">
              <div class="swiper-slide"><img src="/static/images/banner01.jpg"></div>
              <div class="swiper-slide"><img src="/static/images/banner02.jpg"></div>
              <div class="swiper-slide"><img src="/static/images/banner03.jpg"></div>
              <div class="swiper-slide"><img src="/static/images/banner04.jpg"></div>
            </div>
            <div class="swiper-pagination"></div>
         </div>
          <!-- 专题分类 -->
          <div class="clssTitle"><i class="iconfont">&#xe65b;</i><h3>专题分类</h3></div>
           <div class="layui-container">
             <div class="layui-row">
             <div class="layui-col-xs6"><img src="/static/images/home08.jpg"></div>
             <div class="layui-col-xs6"><img src="/static/images/home10.jpg"></div>
           </div>
           </div>
           <!-- 热门推荐 -->
           <div class="clssTitle"><i class="iconfont">&#xe6a6;</i><h3>热门推荐</h3></div>
              
          </div>
</template>

<script>
import "layui-css";
import 'swiper-css';
import Swiper from 'swiper-js';
export default {
  name: 'home',
  data(){
    return{
     plantInfo:"",
    }
  },
     mounted(){
            var swiper = new Swiper('.swiper-container', {
        // 图片间隙
      spaceBetween: 30,
      centeredSlides: true,
    //   播放速度
      autoplay: {
        delay: 2500,
        // 
        disableOnInteraction: false,
      },
    //   
      pagination: {
        el: '.swiper-pagination',
        clickable: true,
      },
    //   左右点击
      navigation: {
        nextEl: '.swiper-button-next',
        prevEl: '.swiper-button-prev',
      },
    });
    },
    created() {
        axios.get('/data/plant.json').then((resp) => {
            this.plantInfo = resp.data;
        });
    }
}
</script>

<style scoped lang="scss">
html, body {
      position: relative;
      height: 100%;
      font-size: 16px;
    }
    body {
      background: #eee;
      font-family: Helvetica Neue, Helvetica, Arial, sans-serif;
      // font-size: 0.7rem;
      color:#000;
      margin: 0;
      padding: 0;
    }
    .swiper-container {
      width: 100%;
      height: auto;
      img{
         width: 100%;
         height: auto;
      }

    }
    .swiper-slide {
      text-align: center;
      font-size: 1.2rem;
      background: #fff;

      /* Center slide text vertically */
      display: -webkit-box;
      display: -ms-flexbox;
      display: -webkit-flex;
      display: flex;
      -webkit-box-pack: center;
      -ms-flex-pack: center;
      -webkit-justify-content: center;
      justify-content: center;
      -webkit-box-align: center;
      -ms-flex-align: center;
      -webkit-align-items: center;
      align-items: center;
    }
    .clssTitle{
      font-family: "san-serif";
      padding-top:20px; 
      i{
        color: pink;
      }
      h3{
        display: inline-block;
        padding-left: 8px;
        font-size: 1.3rem;
      }
    }
    .layui-container{
      padding-top: 20px;
    }
    .layui-row{
      .layui-col-xs6{
        padding-left:5px;
      }
      img{
        width: 100%;
      }
    }
</style>