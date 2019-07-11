<template>
  <div id="app" class="home">
    <div :class="currentBackground">
      <div class="page-banner">
        <div class="top">
          <div class=top_b>
            <div class=slogo><img src="http://www.mjcagt.com/Images/slogo.png" width=161 height=55 /></div>
            <div class=twenzi>  </div>
            <div class=mlogo><img src="http://www.mjcagt.com/Images/mlogo_new.png" width=98 height=55 /></div>
          </div>
        </div>
        <div class="nav">
          <el-menu
            :default-active="defaultOpen[1]"
            :default-openeds="defaultOpen"
            class="el-menu-demo"
            :unique-opened='true'
            mode="horizontal"
            @select="handleSelect"
            background-color="#4946A9"
            text-color="#fff"
            active-text-color="#ffd04b">
            <el-menu-item index="1" class="modify-mean">首页</el-menu-item>
            <el-submenu
              index="3" class="modify-mean">
              <template class="hh" slot="title">公司</template>
              <div class="my-sub-nav">
                  <el-menu-item align="center" class="" index="3-1">二级1</el-menu-item>
                  <el-menu-item align="center" class="" index="3-2">二级2</el-menu-item>
                  <el-menu-item align="center" class="" index="3-3">二级3</el-menu-item>
              </div>
            </el-submenu>
            <el-submenu
              index="2" class="modify-mean">
              <template class="hh" slot="title">机器</template>
              <div class="my-sub-nav">
                <el-submenu index="2-1">
                  <template slot="title" align="center">大气瓶内胆设备</template>
                  <el-menu-item align="center" class="add-bord-sty" index="2-1-1"><a href="#">OSC-9.75</a></el-menu-item>
                  <el-menu-item align="center" class="add-bord-sty" index="2-1-2">OSC-11.100</el-menu-item>
                  <el-menu-item align="center" class="add-bord-sty" index="2-1-3">OSC-16.200</el-menu-item>
                  <el-menu-item align="center" class="add-bord-sty" index="2-1-4">OSC-24.300</el-menu-item>
                  <el-menu-item align="center" class="add-bord-sty" index="2-1-5">OSC-26.300</el-menu-item>
                  <el-menu-item align="center" class="add-bord-sty" index="2-1-6">OSC-28.450</el-menu-item>
                  <el-menu-item align="center" class="add-bord-sty" index="2-1-7">SPT-975-3</el-menu-item>
                  <el-menu-item align="center" class="add-bord-sty" index="2-1-8">SPT-1275-3</el-menu-item>
                </el-submenu>
                <el-submenu index="2-7">
                  <template slot="title" align="center">小气瓶内胆设备</template>
                  <el-menu-item align="center" class="add-bord-sty" index="2-7-1">SPT-9.40</el-menu-item>
                  <el-menu-item align="center" class="add-bord-sty" index="2-7-2">SPT-10.75</el-menu-item>
                  <el-menu-item align="center" class="add-bord-sty" index="2-7-3">SPT-20.150</el-menu-item>
                  <el-menu-item align="center" class="add-bord-sty" index="2-7-4">SPT-26.150</el-menu-item>
                  <el-menu-item align="center" class="add-bord-sty" index="2-7-5">RFN200T-4(RFN350)</el-menu-item>
                </el-submenu>
                <el-submenu index="2-2">
                  <template slot="title" align="center">强力旋压成形机</template>
                  <el-menu-item align="center" class="add-bord-sty" index="2-2-1">F450.2000-4</el-menu-item>
                  <el-menu-item align="center" class="add-bord-sty" index="2-2-2">F450.3000-4</el-menu-item>
                  <el-menu-item align="center" class="add-bord-sty" index="2-2-3">F600.2000-4</el-menu-item>
                  <el-menu-item align="center" class="add-bord-sty" index="2-2-4">F1200.2000-4</el-menu-item>
                  <el-menu-item align="center" class="add-bord-sty" index="2-2-5">F1300.3000-4</el-menu-item>
                </el-submenu>
                <el-submenu index="2-3">
                  <template slot="title" align="center"> SP系列数控旋压机</template>
                  <el-menu-item align="center" class="add-bord-sty" index="2-3-1">SP-32.30</el-menu-item>
                  <el-menu-item align="center" class="add-bord-sty" index="2-3-2">SP-42.50</el-menu-item>
                  <el-menu-item align="center" class="add-bord-sty" index="2-3-3">SP-48.100</el-menu-item>
                  <el-menu-item align="center" class="add-bord-sty" index="2-3-4">SP-48.150-4</el-menu-item>
                  <el-menu-item align="center" class="add-bord-sty" index="2-3-6">SP-72.100</el-menu-item>
                  <el-menu-item align="center" class="add-bord-sty" index="2-3-5">SP-60.100</el-menu-item>
                  <el-menu-item align="center" class="add-bord-sty" index="2-3-7">SP-78.200-3</el-menu-item>
                  <el-menu-item align="center" class="add-bord-sty" index="2-3-8">SP-850-4</el-menu-item>
                </el-submenu>
                <el-submenu index="2-4">
                  <template slot="title" align="center">轮毂旋压机</template>
                  <el-menu-item align="center" class="add-bord-sty" index="2-4-1">WS-700.400-4</el-menu-item>
                  <el-menu-item align="center" class="add-bord-sty" index="2-4-2">WSV-24.150-3</el-menu-item>
                  <el-menu-item align="center" class="add-bord-sty" index="2-4-3">WSV-24.200-3</el-menu-item>
                  <el-menu-item align="center" class="add-bord-sty" index="2-4-1">WSV-26.150-3</el-menu-item>
                  <el-menu-item align="center" class="add-bord-sty" index="2-4-2">WSV-26.150-2</el-menu-item>
                  <el-menu-item align="center" class="add-bord-sty" index="2-4-3">WSV-26.300-3</el-menu-item>
                  <el-menu-item align="center" class="add-bord-sty" index="2-4-3">RFN200T-4(RFN350)</el-menu-item>
                </el-submenu>
                <el-submenu index="2-5">
                  <template slot="title" align="center">客户定制机（铝灯杆）</template>
                  <el-menu-item align="center" class="add-bord-sty" index="2-5-1">FC-10.43F-3</el-menu-item>
                </el-submenu>
                <el-submenu index="2-6">
                  <template slot="title" align="center">客户定制旋压机</template>
                  <el-menu-item align="center" class="add-bord-sty" index="2-6-1">SPC-200.50</el-menu-item>
                  <el-menu-item align="center" class="add-bord-sty" index="2-6-2">SPC-270.150</el-menu-item>
                </el-submenu>
              </div>
            </el-submenu>
            <el-menu-item index="4" class="modify-mean">软件和服务</el-menu-item>
            <el-menu-item index="5" class="modify-mean">信息博采</el-menu-item>
            <el-menu-item index="6" class="modify-mean">视频</el-menu-item>
            <el-menu-item index="7" class="modify-mean">联系方式</el-menu-item>
            <el-submenu
              index="8" class="modify-mean">
              <template class="hh" slot="title">成功案例</template>
              <div class="my-sub-nav">
                <el-menu-item align="center" class="" index="8-1">二级1</el-menu-item>
                <el-menu-item align="center" class="" index="8-2">二级2</el-menu-item>
                <el-menu-item align="center" class="" index="8-3">二级3</el-menu-item>
              </div>
            </el-submenu>
          </el-menu>
        </div>
        <div class="pan">
          <canvas id="canvas1" width="992" height="312"></canvas>
          <div class="line_war">点击线条查看对应型号与成品，建议使用Chrome浏览器或者360等浏览器的极速模式浏览。</div>
          <img src="../assets/product1.png" class="popWin" v-if="visible" alt="" />
        </div>
      </div>
    </div>
    <div class="swiper-container swiperDiv" id="swipper1" ref="mySwiper">
      <div class="swiper-wrapper">
        <div class="swiper-slide swiper-add-1"><img src="../assets/product1.png" alt="这是第1张"></div>
        <div class="swiper-slide swiper-add-2"><img src="../assets/product2.png" alt="这是第2张"></div>
        <div class="swiper-slide swiper-add-3"><img src="../assets/product3.png" alt="这是第3张"></div>
        <div class="swiper-slide swiper-add-4"><img src="../assets/product4.png" alt="这是第4张"></div>
        <div class="swiper-slide swiper-add-5"><img src="../assets/product5.png" alt="这是第5张"></div>
        <div class="swiper-slide swiper-add-6"><img src="../assets/product6.png" alt="这是第6张"></div>
        <div class="swiper-slide swiper-add-7"><img src="../assets/product7.png" alt="这是第7张"></div>
      </div>
    </div>
  </div>
</template>

<style scoped>
  html,body {
    margin: 0;
    padding: 0;
    border: none;
  }
  .swiper-wrapper{
    transition-timing-function: linear;
    -moz-transition-timing-function: linear; /* Firefox 4 */
    -webkit-transition-timing-function: linear; /* Safari 和 Chrome */
    -o-transition-timing-function: linear; /* Opera */
  }
  #app {
    font-family: Avenir, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50
  }

  #nav {
    padding: 30px
  }
  .modify-mean{
    height: 36px !important;
    background: -webkit-gradient(linear, left bottom, left top, from(#190a5d), color-stop(#5251b7), to(#190a5d)) !important;
    background: linear-gradient(0deg, #190a5d, #5251b7, #190a5d) !important;
    line-height: 36px !important;
    width: 138px;
  }
  .modify-mean. el-submenu__title{
    height: 36px !important;
    background: -webkit-gradient(linear, left bottom, left top, from(#190a5d), color-stop(#5251b7), to(#190a5d)) !important;
    background: linear-gradient(0deg, #190a5d, #5251b7, #190a5d) !important;
    line-height: 36px !important;
  }
  #nav a {
    font-weight: 700;
    color: #2c3e50
  }
  #nav a.router-link-exact-active {
    color: #42b983
  }

  .selectBorder {
    border: 4px dotted red !important;
    /*-webkit-animation: borderColor-data-v-2459bd86 2s linear infinite;*/
    /*animation: borderColor-data-v-2459bd86 2s linear infinite;*/
    height: auto
  }
  /*//这是样式修改*/
  .home {
    margin: 0 auto;
    height: auto;
    min-height: 485px
  }
  .add-background{
    background-color: rgba(145, 177, 254, .8);
  }
  .home .page-banner {
    background-color: rgba(145, 177, 254, .8);
    background: url(http://www.mjcagt.com/static/bg2.png) 0% -20% repeat-x;
    background-position-y: -300px;
    background-size: 992px 185px;
    -webkit-backface-visibility: hidden;
    animation: animatedMove-data-v-2459bd86 50s linear infinite;
    -ms-animation: animatedMove-data-v-2459bd86 50s linear infinite;
    -moz-animation: animatedMove-data-v-2459bd86 50s linear infinite;
    -webkit-animation: animatedMove-data-v-2459bd86 50s linear infinite
  }

  .home .top {
    width: 992px;
    height: 92px;
    margin:0 auto;
  }
  .top .top_b {
      width: 992px;
      height: 74px;
      padding-top: 20px;
      margin: 0 auto;
  }
  .top .slogo {
    float: left;
    width: 161px;
    height: 55px;
    padding-left: 30px;
    text-align: left;
  }
  .top .twenzi {
    float: left;
    width: 542px;
    height: 52px;
    text-align: center;
    padding-top: 15px;
  }
  .top .mlogo {
    float: right;
    width: 98px;
    height: 55px;
    padding-right: 26px;
    text-align: right;
  }
  .home .nav {
    padding: 0 4px;
    width:1120px;
    margin:0 auto;
  }

  .home .nav .el-menu-demo {
    height: 36px;
    line-height: 36px;
    margin: 0 auto;
    font-size: 16px;
    border-radius: 6px;
    background: -webkit-gradient(linear, left bottom, left top, from(#190a5d), color-stop(#5251b7), to(#190a5d));
    background: linear-gradient(0deg, #190a5d, #5251b7, #190a5d);
    color: #000 !important
  }

  .home .nav .el-menu-demo .add-bord-sty {
    border: 1px dotted red !important;
    padding: 0 !important
  }

  .home .nav .el-menu-demo .el-menu-item, .home .nav .el-menu-demo > .el-submenu, .home .nav .el-menu-demo > .el-submenu >>> .el-submenu__title {
    height: 36px;
    background: -webkit-gradient(linear, left bottom, left top, from(#190a5d), color-stop(#5251b7), to(#190a5d));
    background: linear-gradient(0deg, #190a5d, #5251b7, #190a5d);
    line-height: 36px;
  }

  .home .nav .el-menu-demo > :first-child {
    border-radius: 6px 0 0 6px
  }

  .home .pan {
    padding-top: 16px;
    width: 100%;
    height: 322px;
    text-align:center;
    margin:0 auto;
    position: relative;
  }

  .home .pan #canvas1 {
    background: url('http://www.mjcagt.com/static/bg3.png') 95px 60px no-repeat;
    position: relative;
  }

  .home .swiperDiv {
    height: 99px;
    margin-top: 8px;
    width: 992px;
  }

  .home .swiperDiv .swiper-wrapper {
    margin-bottom: 30px
  }
  .home .swiperDiv .swiper-wrapper .swiper-slide img {
    height: 82px;
    width: 148px !important;
    display: block;
  }

  .swiper-container-free-mode .swiper-wrapper {
    -webkit-transition-timing-function: linear;
    transition-timing-function: linear
  }

  el-menu--horizontal > .el-menu--popup > .el-submenu, el-menu--horizontal > .el-menu--popup > .el-submenu .el-submenu__title {
    border-bottom: 1px solid #fff
  }

  el-menu--horizontal > .el-menu--popup .my-sub-nav {
    background: #4946a9 !important;
    padding: 0
  }

  el-menu--horizontal > .el-menu--popup .my-sub-nav > .el-submenu, el-menu--horizontal > .el-menu--popup .my-sub-nav >>> .el-menu-item {
    background: #4946a9 !important;
    border-bottom: 1px solid #fff
  }
  .el-submenu .add-bord-sty a{
    text-decoration: none !important;
    out-line: none !important;
    color: #fff;
  }
  .el-submenu .add-bord-sty {
    border: 1px dotted red !important;
    border-radius: 6px;
    min-width: 160px !important;
    padding: 0 !important;
    margin: 0 20px;
    -webkit-animation: borderColor-data-v-2459bd86 2s linear infinite;
    animation: borderColor-data-v-2459bd86 2s linear infinite;
    margin-bottom: 2px
  }

  @-webkit-keyframes animatedMove-data-v-2459bd86 {
    0% {
      background-position: -992px top
    }
    to {
      background-position: 992px top
    }
  }

  @keyframes animatedMove-data-v-2459bd86 {
    0% {
      background-position: -992px top
    }
    to {
      background-position: 992px top
    }
  }

  @-webkit-keyframes borderColor-data-v-2459bd86 {
    0% {
      -webkit-box-shadow: 0 0 8px 4px #83582d;
      box-shadow: 0 0 8px 4px #83582d
    }
    50% {
      -webkit-box-shadow: 0 0 0 0 #83582d;
      box-shadow: 0 0 0 0 #83582d
    }
    to {
      -webkit-box-shadow: 0 0 8px 4px #83582d;
      box-shadow: 0 0 8px 4px #83582d
    }
  }

  @keyframes borderColor-data-v-2459bd86 {
    0% {
      -webkit-box-shadow: 0 0 8px 4px #83582d;
      box-shadow: 0 0 8px 4px #83582d
    }
    50% {
      -webkit-box-shadow: 0 0 0 0 #83582d;
      box-shadow: 0 0 0 0 #83582d
    }
    to {
      -webkit-box-shadow: 0 0 8px 4px #83582d;
      box-shadow: 0 0 8px 4px #83582d
    }
  }
  .add-bord-sty:hover{
    background-color: #fff !important;
    color:rgba(0, 0, 0, 1) !important;
  }
  .add-bord-sty a:link, .el-submenu .add-bord-sty a{
    color:rgba(0, 0, 0, 1) !important;
  }
  .el-submenu__title:hover{
    background-color: #fff !important;
    color:rgba(0, 0, 0, 1) !important;
  }
  .modify-mean .el-submenu__title:hover{
    color:#fff !important;
  }
  .popWin{
    position: absolute;
    top:20%;
    left:65%;
    background: #2c3e50;
    width:150px;
    height:200px;
  }
  .line_war{
    position: absolute;
    top:10%;
    left:20%;
    color: #ffff00;
    font-size: 16px;
    font-weight: 100;
  }
  .swiper-container {
    width: 100%;
    height: 92px;
  }
  .swiper-slide {
    text-align: center;
    font-size: 18px;
    background: #fff;
    height:92px !important;
    -webkit-backface-visibility: hidden !important;
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
  .swiper-wrapper {
    -webkit-transition-timing-function: linear !important; /*之前是ease-out*/
    -moz-transition-timing-function: linear !important;
    -ms-transition-timing-function: linear !important;
    -o-transition-timing-function: linear !important;
    transition-timing-function: linear !important;
    margin: 0 auto !important;
  }
  .unSelectBackground {
    background-color: #4d6dd6;
  }
  .selectBackground {
    background-color: #6587f9;
  }
</style>

<script>
import Swiper from 'swiper/dist/idangerous.swiper'
export default {
  name: 'home',
  data () {
    return {
      defaultOpen: [],
      isChange: false,
      visible: false,
      currentRedIndex: 0,
      currentBackground: 'unSelectBackground',
      context: '',
      flag: false,
      mySwiper: null,
      imageDataFlag: false,
      isDisplayLine: {},
      isDisplayMoveIndex: 0 // 记录鼠标移动到哪个index
    }
  },
  mounted () {
    var _this = this
    var canvas1 = document.getElementById('canvas1')
    var ctx1 = canvas1.getContext('2d')
    this.context = ctx1
    setTimeout(function () {
      _this.drawCanvas(ctx1, { x: 0, y: 0 }, 'noevent')
    }, 0)
    _this.drawCanvas(ctx1, { x: 0, y: 0 }, 'noevent')
    setTimeout(function () {
      _this.mySwiper = new Swiper('#swipper1', {
        loop: true, // 循环模式选项
        // loopAdditionalSlides:3,
        autoplay: {
          delay: 0
        },
        autoplayDisableOnInteraction: false,
        speed: 1600,
        slidesPerView: 6,
        // loopedSlides: 3,
        // spaceBetween: 15,
        freeMode: true,
        roundLengths: true,
        observer: true
      })
      _this.mySwiper.startAutoplay()
    }, 0)
    var timer1 = null
    var timer2 = null
    var comtainer = document.getElementById('swipper1')
    comtainer.addEventListener('mouseenter', function () {
      console.log(':::::mmmm')
      _this.mySwiper.stopAutoplay()
    })
    comtainer.addEventListener('mouseleave', function () {
      console.log(':::::kkkkkk')
      _this.mySwiper.startAutoplay()
    })
    document.addEventListener('mousemove', function (e) {
      e = e || window.event
      var p = _this.getEventPosition(e)
      _this.isDisplayLine = {}
      document.getElementById('canvas1').style.cursor = 'default'
      _this.drawCanvas(ctx1, p, e)
      // timer1 = false
      if (!timer1) {
        timer1 = setTimeout(function () {
          var p = _this.getEventPosition(e)
          // console.log(p)
          _this.drawCanvas(ctx1, p, e)
          timer1 = false
        }, 10)
      }
    }, false)
    document.addEventListener('click', function (e) {
      e = e || window.event
      console.log('isDisplayMoveIndex:')
      console.log(_this.isDisplayMoveIndex)
      console.log(_this.isDisplayLine)
      if (!timer2) {
        timer2 = setTimeout(function () {
          var p = _this.getEventPosition(e)
          console.log(p)
          _this.drawCanvas(ctx1, p, e)
          timer2 = false
        }, 100)
      }
    }, false)
  },
  methods: {
    handleSelect (key, keyPath) {
      var _this = this
      var point = { x: 0, y: 0 }
      if (keyPath && keyPath[1]) {
        _this.currentBackground = 'selectBackground'
        if (keyPath[1] === '2-1') {
          point = { x: 562, y: 120 }
          this.currentRedIndex = 1
        } else if (keyPath[1] === '2-2') {
          point = { x: 588, y: 170 }
          this.currentRedIndex = 2
        } else if (keyPath[1] === '2-3') {
          // point = { x: 788, y: 52 }
          point = { x: 0, y: 0 }
          this.currentRedIndex = 3
        } else if (keyPath[1] === '2-4') {
          point = { x: 780, y: 205 }
          this.currentRedIndex = 4
        } else if (keyPath[1] === '2-5') {
          point = { x: 434, y: 165 }
          this.currentRedIndex = 5
        } else if (keyPath[1] === '2-6') {
          point = { x: 746, y: 235 }
          this.currentRedIndex = 6
        } else if (keyPath[1] === '2-7') {
          point = { x: 678, y: 150 }
          this.currentRedIndex = 7
        }
      }
      this.drawCanvas(this.context, point, '')
      if (key) {
        var meanClick = key.split('-')
        if (meanClick[1]) {
          var cumputedIndex = parseInt(parseInt(meanClick[1]) + 4) % 7
          if (!cumputedIndex) {
            cumputedIndex = 7
          }
          _this.swiperTo(cumputedIndex - 1)
          _this.swiperSelet('swiper-add-' + meanClick[1], parseInt('1'))
        }
      }
    },
    getEventPosition (ev) {
      ev = ev || window.event
      var x, y
      // var scrollX = document.documentElement.scrollLeft || document.body.scrollLeft
      // var scrollY = document.documentElement.scrollTop || document.body.scrollTop
      // x = ev.pageX || ev.clientX + scrollX
      // y = ev.pageY || ev.clientY + scrollY
      if (ev.layerX || ev.layerX === 0) {
        x = parseInt(ev.layerX)
        y = parseInt(ev.layerY)
      } else if (ev.offsetX || ev.offsetX === 0) { // Opera
        x = parseInt(ev.offsetX)
        y = parseInt(ev.offsetY)
      }
      return { x: x, y: y }
    },
    compIePoint (ctx, x, y) {
      if (ctx.isPointInStroke) {
        return ctx.isPointInStroke(x, y)
      } else {
        if (ctx.getImageData(x, y, 1, 1).data[3] !== 0) {
          console.log('getImageData-3:' + ctx.getImageData(x, y, 1, 1).data[3])
          // this.imageDataFlag = !this.imageDataFlag
          return true
        } else {
          console.log('NNNNNNNNNNNN::::' + ctx.getImageData(x, y, 1, 1).data[3])
          // this.imageDataFlag = !this.imageDataFlag
          return false
        }
        // return ctx.isPointInPath(x, y)
      }
    },
    BezierEllipse2 (ctx, x, y, a, b) {
      var k = 0.5522848
      var ox = a * k // 水平控制点偏移量
      var oy = b * k // 垂直控制点偏移量</p> <p> ctx.beginPath();
      ctx.moveTo(x - a, y)
      ctx.bezierCurveTo(x - a, y - oy, x - ox, y - b, x, y - b)
      ctx.bezierCurveTo(x + ox, y - b, x + a, y - oy, x + a, y)
      ctx.bezierCurveTo(x + a, y + oy, x + ox, y + b, x, y + b)
      ctx.bezierCurveTo(x - ox, y + b, x - a, y + oy, x - a, y)
      ctx.closePath()
      ctx.stroke()
    },
    strokeFn (ctx, point, event, meanIndex, currentLineIndex) {
      var _this = this
      _this.isDisplayMoveIndex = currentLineIndex
      if (event && event.type === 'click' && !(_this.compIePoint(ctx, point.x, point.y)) && !_this.isChange) {
        _this.currentRedIndex = 0
        _this.isDisplayLine = {}
      }
      if (_this.compIePoint(ctx, point.x, point.y) || _this.currentRedIndex === currentLineIndex) {
        ctx.save()
        ctx.strokeStyle = 'red'
        if (currentLineIndex !== 0 && currentLineIndex !== ' ') {
          var itemLineObj = {}
          itemLineObj[currentLineIndex] = true
          Object.assign(_this.isDisplayLine, itemLineObj)
        } else {
          _this.isDisplayLine = {}
        }
        document.getElementById('canvas1').style.cursor = 'pointer'
        ctx.stroke()
        ctx.restore()
        if (event && event.type === 'click') {
          _this.currentBackground = 'selectBackground'
          _this.defaultOpen = [ ...meanIndex ]
          _this.isChange = true
          if (_this.compIePoint(ctx, point.x, point.y)) {
            _this.currentRedIndex = currentLineIndex
          }
          var str = _this.defaultOpen[1]
          if (str) {
            var swiperIndex = str.split('-')
            if (swiperIndex[1]) {
              var cumputedIndex = parseInt(parseInt(swiperIndex[1]) + 4) % 7
              if (!cumputedIndex) {
                cumputedIndex = 7
              }
              _this.swiperTo(cumputedIndex - 1)
              _this.swiperSelet('swiper-add-' + swiperIndex[1], parseInt('1'))
            }
          }
        }
      } else {
        ctx.stroke()
        if (event && event.type === 'click' && !_this.isChange) {
          _this.defaultOpen = []
          _this.isChange = true
          _this.currentRedIndex = 0
          _this.isDisplayLine = {}
          _this.currentBackground = 'unSelectBackground'
          _this.swiperSelet('', parseInt('2'))
        }
      }
    },
    drawCanvas (ctx1, p, e) {
      var _this = this
      // 耳朵
      ctx1.clearRect(0, 0, 992, 312)
      ctx1.lineWidth = 2
      ctx1.strokeStyle = '#fff'
      ctx1.beginPath()
      ctx1.moveTo(740, 65)
      ctx1.bezierCurveTo(783, 78, 783, 104, 761, 108)
      if (_this.isDisplayLine[6]) {
        ctx1.lineTo(761, 200)
      } else {
        ctx1.moveTo(761, 200)
      }
      ctx1.bezierCurveTo(784, 206, 784, 232, 740, 236)
      if (_this.isDisplayLine[6]) {
        ctx1.lineTo(740, 65)
        ctx1.moveTo(776, 94)
        ctx1.lineTo(776, 212)
      }
      this.strokeFn(ctx1, p, e, ['2', '2-6'], 6)
      // 圆角矩形
      function Rect (x, y, w, h) {
        return { x: x, y: y, width: w, height: h }
      }

      var Point = function (x, y) {
        return { x: x, y: y }
      }

      function drawRoundedRect (rect, r, ctx, meanArr, currentRedLine) {
        var ptA = Point(rect.x + r, rect.y)
        var ptB = Point(rect.x + rect.width, rect.y)
        var ptC = Point(rect.x + rect.width, rect.y + rect.height)
        var ptD = Point(rect.x, rect.y + rect.height)
        var ptE = Point(rect.x, rect.y)
        ctx.beginPath()

        ctx.moveTo(ptA.x, ptA.y)
        ctx.arcTo(ptB.x, ptB.y, ptC.x, ptC.y, r)
        ctx.arcTo(ptC.x, ptC.y, ptD.x, ptD.y, r)
        ctx.arcTo(ptD.x, ptD.y, ptE.x, ptE.y, r)
        ctx.arcTo(ptE.x, ptE.y, ptA.x, ptA.y, r)
        _this.strokeFn(ctx1, p, e, meanArr, currentRedLine)
      }

      // 小圆角矩形
      var rect = Rect(678, 135, 120, 32)
      drawRoundedRect(rect, 14, ctx1, ['2', '2-7'], 7)

      // 圆柱
      ctx1.beginPath()
      _this.BezierEllipse2(ctx1, 787, 155, 16, 55)
      // ctx1.ellipse(787, 155, 16, 55, 0, 1 / 2 * Math.PI, Math.PI * 5 / 2)
      ctx1.moveTo(786, 100)
      ctx1.lineTo(743, 100)
      ctx1.quadraticCurveTo(725, 155, 743, 210)
      ctx1.lineTo(786, 210)
      this.strokeFn(ctx1, p, e, ['2', '2-4'], 4)

      // 圆弧绘制
      ctx1.beginPath()
      ctx1.moveTo(767, 0)
      ctx1.quadraticCurveTo(840, 151, 767, 312)
      if (_this.isDisplayLine[3]) {
        ctx1.lineTo(767, 0)
      }
      this.strokeFn(ctx1, p, e, ['2', '2-3'], 3)

      // 大圆角矩形绘制
      var rect2 = Rect(530, 120, 270, 60)
      drawRoundedRect(rect2, 20, ctx1, ['2', '2-1'], 1)

      // 腰鼓
      ctx1.beginPath()
      ctx1.moveTo(77, 127)
      ctx1.quadraticCurveTo(430, 146, 942, 127)
      if (_this.isDisplayLine[5]) {
        ctx1.moveTo(942, 127)
        ctx1.lineTo(942, 175)
      } else {
        ctx1.moveTo(942, 175)
      }
      ctx1.quadraticCurveTo(430, 154, 77, 175)
      ctx1.lineTo(77, 127)
      this.strokeFn(ctx1, p, e, ['2', '2-5'], 5)

      // 绘制横虚线
      ctx1.beginPath()
      ctx1.moveTo(37, 151)
      ctx1.lineTo(982, 151)
      ctx1.setLineDash([2])
      ctx1.stroke()
      ctx1.setLineDash([1, 0])
      // 绘制矩形
      ctx1.beginPath()
      ctx1.moveTo(588, 130)
      ctx1.lineTo(838, 130)
      if (_this.isDisplayLine[2]) {
        ctx1.lineTo(838, 170)
      } else {
        ctx1.moveTo(838, 170)
      }
      ctx1.lineTo(588, 170)
      ctx1.moveTo(588, 120)
      ctx1.lineTo(588, 180)
      this.strokeFn(ctx1, p, e, ['2', '2-2'], 2)
      this.isChange = false
    },
    swiperTo (number) {
      this.mySwiper.swipeTo(parseInt(number) - 1, 0, false)
      this.mySwiper.startAutoplay()
    },
    swiperSelet (className, flag) {
      var _this = this
      var domArr2Ope = []
      var domArrOpe = []
      // var domArr2 = document.getElementsByClassName(className)
      // var domArr = document.getElementsByClassName('swiper-slide')
      // var domArrOpe = [ ...domArr ]
      // var domArr2Ope = [ ...domArr2 ]
      // var domArrLength = domArrOpe.length
      var myClassName = className
      domArr2Ope = document.getElementsByClassName(myClassName)
      domArrOpe = document.getElementsByClassName('swiper-slide')
      var domArrLength = domArrOpe.length

      var classPromise = new Promise((resolve, reject) => {
        for (var i = 0; i < domArrLength; i++) {
          if (domArrOpe[i].classList.contains('selectBorder')) {
            domArrOpe[i].classList.remove('selectBorder')
          }
        }
        _this.mySwiper.startAutoplay()
        _this.visible = false
        resolve()
      })
      classPromise.then(result => {
        if (domArr2Ope.length > 0) {
          for (var k = 0; k < domArr2Ope.length; k++) {
            domArr2Ope[k].classList.add('selectBorder')
            _this.mySwiper.stopAutoplay()
            _this.visible = true
          }
        }
      })
    }
  }
}
</script>
