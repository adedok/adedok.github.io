<script setup>
import ImgHL from '@/assets/image/h-l.png'
import ImgLogoB from '@/assets/image/logo-b.png'
import ImgHCT from '@/assets/image/h-c-t.png'
import ImgHCB from '@/assets/image/h-c-b.png'
import ImgWQcH from '@/assets/image/wrap-qc-h.png'
import ImgWCLi1 from '@/assets/image/wrap-c-li.png'
import ImgWCLi2 from '@/assets/image/wrap-c-li2.png'
import ImgWQcB from '@/assets/image/wrap-qc-b.png'


// h-c-b
const open = (type) => {
  if(type == 'privacy'){
    window.open('./privacy.html','_target')
  }else{
    window.open('./terms.html', '_target')
  }
}

</script>

<template>
  <div class="wrap">
    <div class="wrap-header-bg">
      <div class="wrap-header-bg-c">
        <div class="header">
          <div class="header-l">
            <img :src="ImgHL" alt="">
          </div>
          <div class="header-r">
            <p @click="open('terms')">Terms</p>
            <span class="line">|</span>
            <p @click="open('privacy')">Privacy</p>
          </div>
        </div>
        <div class="content">
          <img class="content-t" :src="ImgHCT" alt="" srcset="">
          <p class="content-des">
            Quick AntiVirus that brilliant and practical tool, is developed to assist users in efficiently handling the often-cramped storage space of their Android mobile phones. 
          </p>
          <img class="content-b" :src="ImgHCB" alt="">
        </div>
      </div>
    </div>
    <div class="wrap-con">
      <div class="wrap-con-qc">
        <div class="wrap-con-qc-h">
          <img :src="ImgWQcH">
          <p class="wrap-con-qc-h-des">offers a wealth of features and user - friendly interactive experience.</p>
        </div>
        <ul class="wrap-con-qc-c">
          <li class="wrap-con-qc-c-li">
            <img :src="ImgWCLi1">
            <p>
              quickly locates and deletes space - hogging files. This frees up storage, speeds up your phone, and makes room for new data.
            </p>
          </li>
          <li class="wrap-con-qc-c-li">
            <img :src="ImgWCLi2">
            <p>
              Effortlessly browse through and manage the photos, videos, and audio files stored on your device.
            </p>
          </li>
        </ul>
        <div class="wrap-con-qc-b">
          <img :src="ImgWQcB" alt="">
        </div>
      </div>
    </div>
    <div class="wrap-b"></div>
    <div class="foot">
      <div class="foot-c">
        <img class="foot-c-l" :src="ImgLogoB">
        <div class="foot-c-r">
          <div class="foot-c-r-h">
            <p @click="open('privacy')">Privacy</p>
            <span class="line">|</span>
            <p @click="open('terms')">Terms</p>
          </div>
          <a class="email" href="mailto:info.abedok@gmail.com">
            Contact us：info.abedok@gmail.com
          </a>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped lang="less">
*{
  margin: 0;
  padding: 0;
}
ul, li{
  list-style: none;
}
.wrap{
  width: 100%;
  height: 100%;
  min-height: 100vh;
  &-header-bg{
    background-size: 100% 100%;
    height: 1080px;
    background-image: url(@/assets/image/h-bg.png);
    &-c{
      width: 1200px;
      margin: 0 auto;
      .header{
        display: flex;
        justify-content: space-between;
        align-items: center;
        padding: 19px 4px;
        &-l{
          width: 210px;
          img{
            width: 100%;
          }
        }
        &-r{
          display: flex;
          color: #999999;
          text-align: center;
          font-family: "Roboto";
          font-size: 16px;
          font-style: normal;
          font-weight: 400;
          line-height: normal;
          text-decoration-line: underline;
          text-decoration-style: solid;
          text-decoration-skip-ink: none;
          text-decoration-thickness: auto;
          text-underline-offset: auto;
          text-underline-position: from-font;
          cursor: pointer;
          .line{
            color: #999999;
            text-align: center;
            font-family: "Roboto";
            font-size: 14px;
            font-style: normal;
            font-weight: 400;
            line-height: normal;
            opacity: 0.5;
            margin: 0 16px;
          }
        }
      }
      .content{
        margin-top: 105px;
        text-align: center;
        &-t{
          height: 84px;
          img{
            height: 100%;
          }
        }
        &-des{
          margin: 18px 0 26px;
          color: #a8b3aa;
          text-align: center;
          font-family: "SF Pro Display";
          font-style: normal;
          font-weight: 500;
          line-height: 36px;
          font-size: 24px;
          padding: 0 80px;
        }
        &-b{
          width: 100%;
          img{
            width: 100%;
          }
        }
      }
    }
  }
  &-con{
    width: 1200px;
    margin: 166px auto;
    &-qc{
      &-h{
        img{
          height: 96px;
        }
        &-des{
          margin-top: 8px;
          color: #a8b3aa;
          font-family: "SF Pro Display";
          font-size: 32px;
          font-style: normal;
          font-weight: 500;
          line-height: 36px;
        }
      }
      &-c{
        margin-top: 77px;
        display: flex;
        gap: 50px;
        margin-bottom: 264px;
        &-li{
          width: 550px;
          flex-shrink: 0;
          border-radius: 32px;
          border: 1.5px solid #D8D8D8;
          padding: 27px 27px 33px 27px;
          word-wrap: break-word;
          color: #666666;
          font-family: "SF Pro Display";
          font-size: 28px;
          font-style: normal;
          font-weight: 500;
          line-height: 36px;
          img{
            width: 80px;
            height: 80px;
            margin-bottom: 23px;
          }

        }
      }
      &-b{
        width: 100%;
        img{
          width: 100%;
        }
      }
    }  
  }
  &-b{
    margin-top: -520px;
    height: 470px;
    flex-shrink: 0;
    background: #5BC771;
  }
  &-bot{
    height: 92px;
    img{
      margin-left: 10%;
      width: 684px;
    }
  }
}
.wrap .foot{
  height: 88px;
  flex-shrink: 0;
  background-color: #000;
  &-c{
    height: 100%;
    margin: 0 auto;
    width: 1200px;
    display: flex;
    justify-content: space-between;
    align-items: center;
    &-l{
      width: 204px;
    }
    &-r{
      &-h{
        color: rgba(255, 255, 255, 0.7);
        text-align: right;
        font-family: "Roboto";
        font-size: 14px;
        font-style: normal;
        font-weight: 400;
        line-height: normal;
        margin-bottom: 14px;
        p{
          text-decoration-line: underline;
          text-decoration-style: solid;
          text-decoration-skip-ink: none;
          text-decoration-thickness: auto;
          text-underline-offset: auto;
          text-underline-position: from-font;
          cursor: pointer;
        }
        display: flex;
        flex-direction: row-reverse;
        .line{
          margin: 0 16px;
          text-decoration: unset;
        }
      }
      .email{
        color: rgba(255, 255, 255, 0.7);
        text-align: right;
        font-family: "Roboto";
        font-size: 14px;
        font-style: normal;
        font-weight: 400;
        line-height: normal;
        text-decoration: none;
      }
    }
  }
}
</style>
