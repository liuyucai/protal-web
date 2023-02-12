<template>
  <div class="home">
    <div class="top-nav">
        <div class="top-main">
          <div class="top-left">
            <span class="name-text">One Heart</span>
            <span class="desc-text">做最好的产品</span>
          </div>
          <div class="top-right">
            <div class="topbar-item topbar-item-about">
              关于 One Heart
            </div>
            <div class="operate-panel">
              <div class="topbar-item topbar-item-register">
                <div class="topbar-btn register-btn">
                  免费注册
                </div>
              </div>
              <div class="topbar-item">
                <div class="topbar-btn login-btn">
                  登录
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    <div class="page-main">
        <div class="banner-container">
          <div class="container clearfix">
            <div class="statistics-container fl">
              <div class="statistics-main">
                <div class="statistics-title">一颗心</div>
                <div class="statistics-desc">让产品更简单</div>
              </div>
              <div class="statistics-data">
                <div class="data-num">100</div>
                <div class="data-title">注册用户</div>
              </div>

              <div class="statistics-data">
                <div class="data-num">6</div>
                <div class="data-title">产品数量</div>
              </div>
            </div>
            <div class="swiper-container fr">
              <el-carousel :interval="5000" arrow="always" style="width: 100%;height: 100%">
                <el-carousel-item v-for="item in 4" :key="item">
                  <div text="2xl" justify="center" style="width: 100%;height: 100%">{{ item }}</div>
                </el-carousel-item>
              </el-carousel>
            </div>
          </div>
        </div>
        <div class="product-container">
          <div class="container">
            <div class="container-title">One Heart 产品矩阵</div>
            <div class="container-desc">全业务场景覆盖，快速高效解决项目产品问题</div>
            <div class="product-list">
              <div :class="{'product-item':true,'first':index%3==0}" v-for="(item,index) in productList" :key="index">
                <a href="" target="_blank" class="product-card">
                  <i class="product-icon" :style="{backgroundImage: 'url('+item.icon+')'}"></i>
                  <div class="product-name">{{item.name}}</div>
                  <div class="product-desc">{{item.desc}}</div>
                </a>
              </div>
            </div>
          </div>
        </div>

        <div class="page-footer">
          作者：刘宇才
        </div>
      </div>
  </div>
</template>

<script>
export default {
  // eslint-disable-next-line vue/multi-word-component-names
  name: 'home',

  data() {
    return {
      productList:[
        {
          name:"KeVisual",
          desc:"可视化编辑大屏",
          icon:require("@/assets/images/product/jz.svg"),
        },
        {
          name:"RPA",
          desc:"机器人自动化",
          icon:require("@/assets/images/product/jz.svg"),
        },
        {
          name:"KeVisual",
          desc:"可视化编辑大屏",
          icon:require("@/assets/images/product/jz.svg"),
        },
        {
          name:"RPA",
          desc:"机器人自动化",
          icon:require("@/assets/images/product/jz.svg"),
        }
      ]
    };
  },
  mounted() {

  },
  methods: {

  }

}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped>
  .home{
    width: 100%;
    height: 100%;

    .top-nav{
      position: fixed;
      top: 0;
      width: 100%;
      height: 70px;
      line-height: 70px;
      text-align: left;
      z-index: 10001;
      background-color: #fff;
      font-family: "微软雅黑";
      box-shadow: 0 3px 4px rgb(0 0 0 / 10%);
      box-sizing: border-box;

      .top-main{
        margin: 0 auto;
        max-width: 1380px;
        min-width: 1200px;
        height: 100%;
        .top-left{
          float: left;
        }
        .top-left{
          .name-text{
            font-size: 25px;
            font-weight: bold;
            /*font-family: "comfortaa";*/
          }
          .desc-text{
            margin-left: 20px;
            vertical-align: top;
            padding-top: 6px;
          }
        }

        .top-right{
          float: right;
          .topbar-item{
            display: inline-block;
            margin-right: 35px;
            cursor: pointer;
          }
          .topbar-item.topbar-item-about{
            vertical-align: middle;
          }
          .topbar-item:hover{
            color: #0076fe;
          }
          .operate-panel{
            margin-left: 5px;
            display: inline-block;
            vertical-align: top;
            z-index: 9999;
            font-family: "微软雅黑";

            .topbar-item-register{
              margin-right: 14px;
            }
            .topbar-btn{
              margin: 17px 0;
              display: inline-block;
              vertical-align: middle;
              height: 36px;
              line-height: 34px;
              text-align: center;
              font-size: 14px;
              border-radius: 28px;
              box-sizing: border-box;
              cursor: pointer;
            }
            .topbar-btn.register-btn{
              border: 1px solid #0076fe;
              background-color: #0076fe;
              color: #fff;
              width: 112px;
            }
            .topbar-btn.register-btn:hover{
              background-color: #2288fe;
              border-color: #5776ff;
              color: #fff;
              transition: background-color .3s,border-color .3s;
            }

            .topbar-btn.login-btn{
              border: 1px solid #dcdcdc;
              color: #333;
              background: #fff;
              width: 72px;
            }
            .topbar-btn.login-btn:hover{
              border-color: #0076fe;
              color: #0076fe;
              transition: background-color .3s,border-color .3s;
            }
          }
        }
      }
    }
    .page-main{
      padding-top: 70px;
      .banner-container{
        height: 570px;
        background: url('@/assets/images/bg1.png') no-repeat center;

        .container {
          padding-top: 70px;
          .statistics-container{
            .statistics-main{
              margin-top: 17px;
              margin-bottom: 12px;
              font-size: 35px;
              line-height: 50px;

            }
            .statistics-data{
              margin-top: 30px;
              vertical-align: middle;
              line-height: 1;

              .data-num {
                height: 50px;
                line-height: 50px;
                color: #0076fe;
                font-size: 40px;
                font-family: HelveticaNeueLTPro,微软雅黑;
                font-weight: normal;
              }
              .data-title{
                margin-top: 5px;
                color: #757982;
                font-size: 14px;
              }
            }
          }

          .swiper-container{
            position: relative;
            width: 850px;
            height: 430px;
            box-shadow: 0 10px 36px 2px rgb(68 93 127 / 16%);
            border-radius: 4px;

            ::v-deep .el-carousel__container{
              width: 100%;
              height: 100%;
            }
            .el-carousel__item:nth-child(2n) {
              background-color: #99a9bf;
            }

            .el-carousel__item:nth-child(2n + 1) {
              background-color: #d3dce6;
            }
          }
        }
      }
      .product-container{
        height: 700px;
        background: url('@/assets/images/bg2.png') no-repeat center;

        .container-title{
          height: 120px;
          line-height: 28px;
          padding-top: 60px;
          font-size: 30px;
          font-weight: 300;
          text-align: center;
          box-sizing: border-box;
        }
        .container-desc{
          position: relative;
          top: -23px;
          height: 32px;
          line-height: 32px;
          text-align: center;
          font-size: 15px;
          font-weight: 400;
          color: #999;
        }

        .product-list{
          margin-top: 18px;
          .product-item{
            position: relative;
            margin-left: 60px;
            margin-bottom: 30px;
            display: inline-block;
            width: 360px;
            height: 90px;
            background: #fff;
            box-shadow: 0 4px 20px 5px rgb(68 93 127 / 10%);
            border-radius: 4px;
            transition: transform .3s ease,box-shadow .3s ease;

            .product-card {
              display: block;
              width: 100%;
              height: 100%;
              transition: filter .3s,transform .3s;
              padding: 20px 20px 20px 90px;
              box-sizing: border-box;
              .product-icon{
                position: absolute;
                top: 20px;
                left: 20px;
                width: 50px;
                height: 50px;
                background-size: 100% 100%;
              }
              .product-name {
                line-height: 20px;
                font-size: 18px;
                color: #333;
              }
              .product-desc {
                margin-top: 12px;
                color: #999;
                font-size: 13px;
                /*opacity: .7;*/
                /*filter: alpha(opacity=70);*/
              }
            }
          }
          .product-item.first{
            margin-left: 0;
          }
        }
      }

      .container{
        margin: 0 auto;
        width: 1200px;
      }

      .page-footer{
        background-color: #282828;
        font-family: Microsoft YaHei;
        font-weight: 400;
        color: #5d5d5d;
        font-size: 14px;
        text-align: center;
      }
    }

  }
</style>
