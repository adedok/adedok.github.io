<script setup>
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
    <div class="wrap-con">
      <div class="wrap-con-top">
        <img src="@/assets/image/top.png">
      </div>
      <div class="wrap-con-t">
        <div class="left">
          <!-- <p class="graph"></p> -->
          <img class="graph" src="@/assets/image/icon.png">
          <p class="tit">Enjoy <span>Pure Manager</span></p>
          <p class="desc">Pure Manager that brilliant and practical tool, is developed to assist users in efficiently handling the often-cramped storage space of their Android mobile phones. By virtue of its robust and innovative functions, it can meticulously take care of your device's complex file system, numerous apps as well as precious data, and at the same time offer you a truly straightforward and highly efficient experience.</p>
        </div>
        <img class="rig" src="@/assets/image/cont.png">
      </div>
      <div class="wrap-con-b">
        <img src="@/assets/image/bottom.png">
      </div>
    </div>
    <div class="foot">
      <div class="foot-h">
        <p @click="open('terms')">Terms</p>
        <span class="line">|</span>
        <p @click="open('privacy')">Privacy</p>
      </div>
      <a class="email" href="mailto:info.abedok@gmail.com">
        Contact us：info.abedok@gmail.com
      </a>
    </div>
  </div>
</template>

<style scoped lang="less">
*{
  margin: 0;
  padding: 0;
}
.wrap{
  width: 100%;
  height: 100%;
  min-height: 100vh;
  overflow-y: auto;
  &-con{
    &-top{
      margin-bottom: 148px;
      display: flex;
      justify-content: flex-end;
      img{
        width: 689px;
        margin-right: 10%;
      }
    }
    &-t{
      display: flex;
      justify-content: center;
      gap: 32px;
      margin-bottom: 62px;
      .left{
        width: 524px;
        .graph{
          width: 80px;
          height: 80px;
          flex-shrink: 0;
          border-radius: 12px;
          // background: #40BA6D;
          margin-bottom: 40px;
        }
        .tit{
          color: #000000;
          font-family: "SF Pro Display";
          font-size: 40px;
          font-style: normal;
          font-weight: 800;
          margin-bottom: 20px;
          display: flex;
          span{
            margin-left: 10px;
            // height: 56px;
            flex-shrink: 0;
            border-radius: 12px;
            background: #0ebe5a5c;
            padding: 4px 8px;
          }
        }
        .desc{
          color: #999999;
          font-family: "Roboto";
          font-size: 16px;
          font-style: normal;
          font-weight: 400;
          line-height: 24px;
        }
      }
      .rig{
        width: 620px;
        height: auto;
      }
    }
    &-b{
      display: flex;
      img{
        margin-left: 10%;
        width: 684px;
        height: 100%;
      }
    }
  }
}
.wrap .foot{
  height: 88px;
  flex-shrink: 0;
  background-color: #000;
  display: flex;
  justify-content: center;
  flex-direction: column;
  align-items: center;
  &-h{
    color: #ffffff;
    text-align: center;
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
    .line{
      margin: 0 16px;
      text-decoration: unset;
    }
  }
  .email{
    color: #ffffff;
    text-align: center;
    font-family: "Roboto";
    font-size: 14px;
    font-style: normal;
    font-weight: 400;
    line-height: normal;
    text-decoration: none;
  }
}
</style>
