<template>
  <div id="app" class="home">
    <div :class="currentBackground">
      <div class="page-banner">
        <div class="top">
          <div class=top_b>
            <div class=slogo><img src="http://www.mjcagt.com/Images/slogo.png" width=161 height=55 /></div>
            <div class=twenzi>  </div>
            <div class=mlogo><a href="http://mjcengineering.com/" target="_blank"><img src="http://www.mjcagt.com/Images/mlogo_new.png" width=98 height=55 /></a></div>
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
            ref="mean"
            active-text-color="#ffd04b">
            <el-menu-item index="1" class="modify-mean" :class="{'activeFristBg':menu_index}"><a href="http://www.mjcagt.com" target="_blank">首页</a></el-menu-item>
            <el-submenu
              index="3" class="modify-mean">
              <template class="hh" slot="title"><a href="http://www.mjcagt.com/about/showarticle.asp?articleid=24" target="_blank">公司</a></template>
              <div class="my-sub-nav">
                <el-menu-item align="center" class="twoj" index="3-1"><a href="http://www.mjcagt.com/about/showarticle.asp?articleid=24" target="_blank">公司简介</a></el-menu-item>
                <el-menu-item align="center" class="twoj" index="3-2"><a href="http://www.mjcagt.com/about/showarticle.asp?articleid=25" target="_blank">美国MJC简介</a></el-menu-item>
                <el-menu-item align="center" class="twoj" index="3-3"><a href="http://www.mjcagt.com/about/showarticle.asp?articleid=41" target="_blank">荣誉&资质</a></el-menu-item>
              </div>
            </el-submenu>
            <el-submenu
              index="2" class="modify-mean">
              <template class="hh act" slot="title"><a href="http://www.mjcagt.com/product/index.html" target="_blank">机器</a></template>
              <div class="my-sub-nav">
                <el-submenu index="2-1">
                  <template slot="title" align="center"><a href="http://www.mjcagt.com/product/index.html" target="_blank">大气瓶内胆设备</a></template>
                  <el-menu-item align="center" class="add-bord-sty" index="2-1-1"><a href="http://www.mjcagt.com/product/ShowArticle.asp?ArticleID=33" target="_blank">OSC-9.75</a></el-menu-item>
                  <el-menu-item align="center" class="add-bord-sty" index="2-1-2"><a href="http://www.mjcagt.com/product/ShowArticle.asp?ArticleID=33" target="_blank">OSC-11.100</a></el-menu-item>
                  <el-menu-item align="center" class="add-bord-sty" index="2-1-3"><a href="http://www.mjcagt.com/product/ShowArticle.asp?ArticleID=33" target="_blank">OSC-16.200</a></el-menu-item>
                  <el-menu-item align="center" class="add-bord-sty" index="2-1-4"><a href="http://www.mjcagt.com/product/ShowArticle.asp?ArticleID=33" target="_blank">OSC-24.300</a></el-menu-item>
                  <el-menu-item align="center" class="add-bord-sty" index="2-1-5"><a href="http://www.mjcagt.com/product/ShowArticle.asp?ArticleID=33" target="_blank">OSC-26.300</a></el-menu-item>
                  <el-menu-item align="center" class="add-bord-sty" index="2-1-6"><a href="http://www.mjcagt.com/product/ShowArticle.asp?ArticleID=33" target="_blank">OSC-28.450</a></el-menu-item>
                  <el-menu-item align="center" class="add-bord-sty" index="2-1-7"><a href="http://www.mjcagt.com/product/ShowArticle.asp?ArticleID=38" target="_blank">SPT-975-3</a></el-menu-item>
                  <el-menu-item align="center" class="add-bord-sty" index="2-1-8"><a href="http://www.mjcagt.com/product/ShowArticle.asp?ArticleID=38" target="_blank">SPT-1275-3</a></el-menu-item>
                </el-submenu>
                <el-submenu index="2-7">
                  <template slot="title" align="center"><a href="http://www.mjcagt.com/product/index.html" target="_blank">小气瓶内胆设备</a></template>
                  <el-menu-item align="center" class="add-bord-sty" index="2-7-1"><a href="http://www.mjcagt.com/product/ShowArticle.asp?ArticleID=38" target="_blank">SPT-9.40</a></el-menu-item>
                  <el-menu-item align="center" class="add-bord-sty" index="2-7-2"><a href="http://www.mjcagt.com/product/ShowArticle.asp?ArticleID=38" target="_blank">SPT-10.75</a></el-menu-item>
                  <el-menu-item align="center" class="add-bord-sty" index="2-7-3"><a href="http://www.mjcagt.com/product/ShowArticle.asp?ArticleID=38" target="_blank">SPT-20.150</a></el-menu-item>
                  <el-menu-item align="center" class="add-bord-sty" index="2-7-4"><a href="http://www.mjcagt.com/product/ShowArticle.asp?ArticleID=38" target="_blank">SPT-26.150</a></el-menu-item>
                  <el-menu-item align="center" class="add-bord-sty" index="2-7-5"><a href="http://www.mjcagt.com/product/ShowArticle.asp?ArticleID=38" target="_blank">RFN200T-4(RFN350)</a></el-menu-item>
                </el-submenu>
                <el-submenu index="2-2">
                  <template slot="title" align="center"><a href="http://www.mjcagt.com/product/index.html" target="_blank">强力旋压成形机</a></template>
                  <el-menu-item align="center" class="add-bord-sty" index="2-2-1"><a href="http://www.mjcagt.com/product/ShowArticle.asp?ArticleID=77" target="_blank">F450.2000-4</a></el-menu-item>
                  <el-menu-item align="center" class="add-bord-sty" index="2-2-2"><a href="http://www.mjcagt.com/product/ShowArticle.asp?ArticleID=76" target="_blank">F450.3000-4</a></el-menu-item>
                  <el-menu-item align="center" class="add-bord-sty" index="2-2-3">F600.2000-4</el-menu-item>
                  <el-menu-item align="center" class="add-bord-sty" index="2-2-4"><a href="http://www.mjcagt.com/product/ShowArticle.asp?ArticleID=78" target="_blank">F1200.2000-4</a></el-menu-item>
                  <el-menu-item align="center" class="add-bord-sty" index="2-2-5">F1300.3000-4</el-menu-item>
                </el-submenu>
                <el-submenu index="2-3">
                  <template slot="title" align="center"> <a href="http://www.mjcagt.com/product/index.html" target="_blank">SP系列数控旋压机</a></template>
                  <el-menu-item align="center" class="add-bord-sty" index="2-3-1"><a href="http://www.mjcagt.com/product/ShowArticle.asp?ArticleID=35" target="_blank">SP-32.30</a></el-menu-item>
                  <el-menu-item align="center" class="add-bord-sty" index="2-3-2"><a href="http://www.mjcagt.com/product/ShowArticle.asp?ArticleID=35" target="_blank">SP-42.50</a></el-menu-item>
                  <el-menu-item align="center" class="add-bord-sty" index="2-3-3"><a href="http://www.mjcagt.com/product/ShowArticle.asp?ArticleID=35" target="_blank">SP-48.100</a></el-menu-item>
                  <el-menu-item align="center" class="add-bord-sty" index="2-3-4"><a href="http://www.mjcagt.com/product/ShowArticle.asp?ArticleID=35" target="_blank">SP-48.150-4</a></el-menu-item>
                  <el-menu-item align="center" class="add-bord-sty" index="2-3-6"><a href="http://www.mjcagt.com/product/ShowArticle.asp?ArticleID=35" target="_blank">SP-72.100</a></el-menu-item>
                  <el-menu-item align="center" class="add-bord-sty" index="2-3-5"><a href="http://www.mjcagt.com/product/ShowArticle.asp?ArticleID=35" target="_blank">SP-60.100</a></el-menu-item>
                  <el-menu-item align="center" class="add-bord-sty" index="2-3-7"><a href="http://www.mjcagt.com/product/ShowArticle.asp?ArticleID=35" target="_blank">SP-78.200-3</a></el-menu-item>
                  <el-menu-item align="center" class="add-bord-sty" index="2-3-8"><a href="http://www.mjcagt.com/product/ShowArticle.asp?ArticleID=35" target="_blank">SP-850-4</a></el-menu-item>
                </el-submenu>
                <el-submenu index="2-4">
                  <template slot="title" align="center"><a href="http://www.mjcagt.com/product/index.html" target="_blank">轮毂旋压机</a></template>
                  <el-menu-item align="center" class="add-bord-sty" index="2-4-1"><a href="http://www.mjcagt.com/product/ShowArticle.asp?ArticleID=37" target="_blank">WS-700.400-4</a></el-menu-item>
                  <el-menu-item align="center" class="add-bord-sty" index="2-4-2"><a href="http://www.mjcagt.com/product/ShowArticle.asp?ArticleID=36" target="_blank">WSV-24.150-3</a></el-menu-item>
                  <el-menu-item align="center" class="add-bord-sty" index="2-4-3"><a href="http://www.mjcagt.com/product/ShowArticle.asp?ArticleID=36" target="_blank">WSV-24.200-3</a></el-menu-item>
                  <el-menu-item align="center" class="add-bord-sty" index="2-4-1"><a href="http://www.mjcagt.com/product/ShowArticle.asp?ArticleID=36" target="_blank">WSV-26.150-3</a></el-menu-item>
                  <el-menu-item align="center" class="add-bord-sty" index="2-4-2"><a href="http://www.mjcagt.com/product/ShowArticle.asp?ArticleID=36" target="_blank">WSV-26.150-2</a></el-menu-item>
                  <el-menu-item align="center" class="add-bord-sty" index="2-4-3"><a href="http://www.mjcagt.com/product/ShowArticle.asp?ArticleID=36" target="_blank">WSV-26.300-3</a></el-menu-item>
                  <el-menu-item align="center" class="add-bord-sty" index="2-4-3">RFN200T-4(RFN350)</el-menu-item>
                </el-submenu>
                <el-submenu index="2-5">
                  <template slot="title" align="center"><a href="http://www.mjcagt.com/product/index.html" target="_blank">客户定制机（铝灯杆）</a></template>
                  <el-menu-item align="center" class="add-bord-sty" index="2-5-1">FC-10.43F-3</el-menu-item>
                </el-submenu>
                <el-submenu index="2-6">
                  <template slot="title" align="center"><a href="http://www.mjcagt.com/product/index.html" target="_blank">客户定制旋压机</a></template>
                  <el-menu-item align="center" class="add-bord-sty" index="2-6-1">SPC-200.50</el-menu-item>
                  <el-menu-item align="center" class="add-bord-sty" index="2-6-2">SPC-270.150</el-menu-item>
                </el-submenu>
              </div>
            </el-submenu>
            <!-- <el-menu-item index="4" class="modify-mean">软件和服务</el-menu-item> -->
            <el-submenu
              index="4" class="modify-mean">
              <template class="hh" slot="title"><a href="http://www.mjcagt.com/mjcsoft/" target="_blank">软件和服务</a></template>
              <div class="my-sub-nav">
                <el-menu-item align="center" class="twoj" index="4-1"><a href="http://www.mjcagt.com/mjcsoft/#spincad" target="_blank">SpinCAD®</a></el-menu-item>
                <el-menu-item align="center" class="twoj" index="4-2"><a href="http://www.mjcagt.com/mjcsoft/#gaizao" target="_blank">机器改造</a></el-menu-item>
                <el-menu-item align="center" class="twoj" index="4-3"><a href="http://www.mjcagt.com/mjcsoft/#shengji" target="_blank">机器数码升级</a></el-menu-item>
                <el-menu-item align="center" class="twoj" index="4-4"><a href="http://www.mjcagt.com/mjcsoft/#jiqiren" target="_blank">配套机器人</a></el-menu-item>
                <el-menu-item align="center" class="twoj" index="4-5"><a href="http://www.mjcagt.com/mjcsoft/#yeya" target="_blank">绿色液压动力</a></el-menu-item>
              </div>
            </el-submenu>
            <el-menu-item index="5" class="modify-mean"><a href="http://www.mjcagt.com/article/" target="_blank">信息博采</a></el-menu-item>
            <el-menu-item index="6" class="modify-mean"><a href="http://www.mjcagt.com/productcase/" target="_blank">视频</a></el-menu-item>
            <el-menu-item index="7" class="modify-mean"><a href="http://www.mjcagt.com/about/Showarticle.asp?articleID=82" target="_blank">联系方式</a></el-menu-item>
            <!-- <el-submenu
              index="8" class="modify-mean">
              <template class="hh" slot="title">成功案例</template>
              <div class="my-sub-nav">
                <el-menu-item align="center" class="twoj" index="8-1"><a href="http://www.mjcagt.com/case/Showarticle.asp?articleID=85">重庆宝钢案例</a></el-menu-item>
                <el-menu-item align="center" class="twoj" index="8-2"><a href="http://www.mjcagt.com/case/Showarticle.asp?articleID=131">柳州轮毂案例</a></el-menu-item>
                <el-menu-item align="center" class="twoj" index="8-3"><a href="http://www.mjcagt.com/case/Showarticle.asp?articleID=134">张家港富瑞氢能案例</a></el-menu-item>
              </div>
            </el-submenu> -->
          </el-menu>
        </div>
        <div class="pan">
          <canvas id="canvas1" width="992" height="312"></canvas>
          <div class="line_war">点击线条查看对应型号与成品，建议使用Chrome浏览器或者360等浏览器的极速模式浏览。</div>
          <img :src="img_src" class="popWin" v-if="visible" alt="" />
        </div>
      </div>
    </div>
    <div class="swiper-container swiperDiv" id="swipper1" ref="mySwiper">
      <div class="swiper-wrapper">
        <div class="swiper-slide swiper-add-1"><a href="http://www.mjcagt.com/product/ShowArticle.asp?ArticleID=33" target="_blank"><div class="pic_shadow"><span>大气瓶</span></div></a><img src="../assets/product11.png" alt="钢瓶"></div>
        <div class="swiper-slide swiper-add-2"><a href="http://www.mjcagt.com/product/ShowArticle.asp?ArticleID=77" target="_blank"><div class="pic_shadow"><span>灯杆</span></div></a><img src="../assets/product12.png" alt="灯杆"></div>
        <div class="swiper-slide swiper-add-3"><a href="http://www.mjcagt.com/product/ShowArticle.asp?ArticleID=36" target="_blank"><div class="pic_shadow"><span>碟形/封头</span></div></a><img src="../assets/product13.png" alt="车轮毂"></div>
        <div class="swiper-slide swiper-add-4"><a href="http://www.mjcagt.com/product/ShowArticle.asp?ArticleID=36" target="_blank"><div class="pic_shadow"><span>车轮毂</span></div></a><img src="../assets/product14.png" alt="刹车鼓"></div>
        <div class="swiper-slide swiper-add-5"><a href="http://www.mjcagt.com/product/ShowArticle.asp?ArticleID=76" target="_blank"><div class="pic_shadow"><span>灯杆</span></div></a><img src="../assets/product15.png" alt="灯杆"></div>
        <div class="swiper-slide swiper-add-6"><a href="#" target="_blank"><div class="pic_shadow"><span>飞机发动机唇</span></div></a><img src="../assets/product16.png" alt="飞机发动机唇"></div>
        <div class="swiper-slide swiper-add-7"><a href="http://www.mjcagt.com/product/ShowArticle.asp?ArticleID=35" target="_blank"><div class="pic_shadow"><span>小气瓶/桶形</span></div></a><img src="../assets/product17.png" alt="桶形锥形钢制品"></div>
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
  a{
    text-decoration:none;
    cursor: pointer;
    color: #fff;
  }
  .swiper-wrapper{
    transition-timing-function: linear;
    -moz-transition-timing-function: linear; /* Firefox 4 */
    -webkit-transition-timing-function: linear; /* Safari 和 Chrome */
    -o-transition-timing-function: linear; /* Opera */
  }
  #app {
    font-family: "Microsoft Yahei","PingFang SC","STXihei", Helvetica,Arial,sans-serif;
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
  .modify-mean:hover{
    background: url('../assets/menu_bg.png') no-repeat center !important;
  }
  .activeFristBg{
    background: url('../assets/menu_bg.png') no-repeat center !important;
  }
  .modify-mean. el-submenu__title{
    height: 36px !important;
    background: -webkit-gradient(linear, left bottom, left top, from(#190a5d), color-stop(#5251b7), to(#190a5d)) !important;
    background: linear-gradient(0deg, #190a5d, #5251b7, #190a5d) !important;
    line-height: 36px !important;
  }
  .modify-mean.el-submenu.act{
    background:#fff;
  }
  #nav a {
    font-weight: 700;
    color: #2c3e50
  }
  #nav a.router-link-exact-active {
    color: #42b983
  }

  .selectBorder {
    border: 4px red solid !important;
    -webkit-animation: borderColor-data-v-2459bd86 2s linear infinite;
    animation: borderColor-data-v-2459bd86 2s linear infinite;
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
    width:1010px;
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
    height: 110px;
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
      -webkit-box-shadow: 0 0 8px 4px #ffea00;
      box-shadow: 0 0 5px rgba(255, 0, 0, .2), inset 0 0 5px rgba(255, 0, 0, .1), 0 1px 0 #ffea00;
    }
    50% {
      -webkit-box-shadow: 0 0 0 0 #ff0000;
      box-shadow: 0 0 20px rgba(255, 0, 0, 1), inset 0 0 10px rgba(255, 0, 0, .4), 0 1px 0 #ff0000;
    }
    to {
      -webkit-box-shadow: 0 0 8px 4px #ffea00;
      box-shadow: 0 0 5px rgba(255, 0, 0, .2), inset 0 0 5px rgba(255, 0, 0, .1), 0 1px 0 #ffea00;
    }
  }

  @keyframes borderColor-data-v-2459bd86 {
    0% {
      -webkit-box-shadow: 0 0 8px 4px #ffea00;
      box-shadow: 0 0 5px rgba(255, 0, 0, .2), inset 0 0 5px rgba(255, 0, 0, .1), 0 1px 0 #ffea00;
    }
    50% {
      -webkit-box-shadow: 0 0 0 0 #ff0000;
      box-shadow: 0 0 20px rgba(255, 0, 0, 1), inset 0 0 10px rgba(255, 0, 0, .4), 0 1px 0 #ff0000;
    }
    to {
      -webkit-box-shadow: 0 0 8px 4px #ffea00;
      box-shadow: 0 0 5px rgba(255, 0, 0, .2), inset 0 0 5px rgba(255, 0, 0, .1), 0 1px 0 #ffea00;
    }
  }
    .twoj{
    text-align: left;
  }
  .twoj a{
    color: #fff;
    text-align: left;
   }
  .add-bord-sty:hover {
    background-color: #fff !important;
    color:rgba(0, 0, 0, 1) !important;
  }
  .add-bord-sty:hover a{
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
    /* background: #2c3e50; */
    border:4px #fff solid;
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
    font-size: 15px;
    margin-right: 5px;
    height:98px !important;
    position: relative;
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
  .swiper-slide img{
    border: 4px #32478c solid;
  }
  /*.control-shadow .pic_shadow{*/
    /*display: none;*/
  /*}*/
  .pic_shadow span{
    line-height: 82px;
    display: none;
  }
  .control-shadow .pic_shadow span{
    line-height: 82px;
    display: block !important;
  }
  .control-shadow .pic_shadow{
    width: 100%;
    height:100%;
    position: absolute;
    top:0;
    left:0;
    display: block;
    background: rgba(0, 0, 0, .5);
    color: #fff;
  }
  .swiper-slide .pic_shadow span{
    line-height: 82px;
    display: none;
  }
  .swiper-slide:hover .pic_shadow span{
    line-height: 82px;
    display: block !important;
  }
  .swiper-slide:hover .pic_shadow{
    width: 100%;
    height:100%;
    position: absolute;
    top:0;
    left:0;
    display: block;
    background: rgba(0, 0, 0, .5);
    color: #fff;
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
import Swiper from 'swiper/dist/js/swiper'
export default {
  name: 'home',
  data () {
    return {
      defaultOpen: [],
      isChange: false,
      visible: false,
      bannerPicIndex: 0,
      img_src: '',
      menu_index: true,
      currentRedIndex: 0,
      currentBackground: 'unSelectBackground',
      context: '',
      flag: false,
      mySwiper: null,
      imageDataFlag: false,
      isDisplayLine: {},
      isDisplayMoveIndex: 0, // 记录鼠标移动到哪个index
      swiperMoveTimer: null
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
          delay: 0,
          stopOnLastSlide: false,
          disableOnInteraction: true
        },
        // autoplayDisableOnInteraction: false,
        speed: 1600,
        slidesPerView: 6,
        // loopedSlides: 3,
        spaceBetween: 15,
        freeMode: true,
        // roundLengths: true,
        observer: true
      })
      _this.mySwiper.autoplay.start()
    }, 0)
    var timer1 = null
    var timer2 = null
    var comtainer = document.getElementsByClassName('swiper-wrapper')[0]
    comtainer.addEventListener('mouseenter', function (e) {
      e = e || event
      console.log(':::::mmmm')
      console.log(e)
      console.log(e.target)
      this.swiperMoveTimer = setTimeout(function () {
        _this.mySwiper.autoplay.stop()
      }, 0)
    })
    comtainer.addEventListener('mouseleave', function (e) {
      e = e || event
      console.log(':::::kkkkkk:')
      console.log(e.target)
      _this.mySwiper.autoplay.start()
      if (this.swiperMoveTimer) {
        clearTimeout(this.swiperMoveTimer)
        _this.mySwiper.autoplay.start()
      }
    })
    document.addEventListener('mousemove', function (e) {
      e = e || window.event
      var p = _this.getEventPosition(e)
      _this.isDisplayLine = {}
      document.getElementById('canvas1').style.cursor = 'default'
      _this.drawCanvas(ctx1, p, e)
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
      if (key !== '1') {
        this.menu_index = false
      }
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
          // console.log('_this.defaultOpen:')
          // console.log(_this.defaultOpen)
          // console.log(_this.$refs.mean)
          // var domIndex = _this.defaultOpen[1].split('-')
          // console.log(_this.$refs.mean.$children[_this.defaultOpen[0]].$children[domIndex[1]].style)
          // _this.$refs.mean.$children[_this.defaultOpen[0]].$children[domIndex[1]].style.cssText = 'border-bottom-color: transparent; color: rgb(255, 255, 255); background-color: rgb(73, 70, 169);'
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
      this.mySwiper.slideTo(parseInt(number) - 1, 0, false)
      this.mySwiper.autoplay.start()
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
      if (className) {
        var picIndex = className.split('-')
        if (picIndex[2]) {
          _this.bannerPicIndex = picIndex[2]
          _this.img_src = require('@/assets/product' + this.bannerPicIndex + '.png')
        }
      }
      domArr2Ope = document.getElementsByClassName(myClassName)
      domArrOpe = document.getElementsByClassName('swiper-slide')
      var domArrLength = domArrOpe.length

      var classPromise = new Promise((resolve, reject) => {
        for (var i = 0; i < domArrLength; i++) {
          if (domArrOpe[i].classList.contains('selectBorder')) {
            domArrOpe[i].classList.remove('selectBorder')
          }
          if (domArrOpe[i].classList.contains('control-shadow')) {
            domArrOpe[i].classList.remove('control-shadow')
          }
        }
        _this.mySwiper.autoplay.start()
        _this.visible = false
        resolve()
      })
      classPromise.then(result => {
        if (domArr2Ope.length > 0) {
          for (var k = 0; k < domArr2Ope.length; k++) {
            domArr2Ope[k].classList.add('selectBorder', 'control-shadow')
            console.log(':::::mmmm')
            _this.mySwiper.autoplay.stop()
            _this.visible = true
          }
        }
      })
    }
  }
}
</script>
