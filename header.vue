<template>
      <div>
          <!-- 顶部搜索框开始 -->
          
            <div class="div_sech" fixed>
              <form action="" target="frameFile">
                <mt-search v-model="value" cancel-text="搜索"  placeholder="搜索" @keyup.enter.native="searchData">
                </mt-search></form>
              <iframe name='frameFile' style="display: none;"></iframe>
         </div>
       <!--顶部搜索框结束  -->
       <!--顶部选项开始 -->
          <div class="second">
            <ul>
              <li>
                <img src="../../assets/asset/美食.png">
                <p>美食</p>
              </li>
             <li>
                <img src="../../assets/asset/饮品.png">
                <p>饮品</p>
              </li>
              <li>
                <img src="../../assets/asset/超市.png">
                <p>超市</p>
              </li>
              <li>
                <img src="../../assets/asset/精选.png">
                <p>精选</p>
              </li>
            </ul>
          </div>
          <div class="seconds">
              <ul>
              <li>
                <img src="../../assets/asset/水果.png">
                <p>生鲜果蔬</p>
              </li>
             <li>
                <img src="../../assets/asset/全部.png">
                <p>全部商家</p>
              </li>
              <li>
                <img src="../../assets/asset/免费.png">
                <p>免费配送</p>
              </li>
              <li>
                <img src="../../assets/asset/新.png">
                <p>新商家</p>
              </li>
            </ul>
          </div>
       <!--顶部选项结束  -->
       <!--轮播图开始  -->
      <div class="secondas">
         <mt-swipe :auto=4000 :showIndicators="true" class=" mint-swipe">
          <mt-swipe-item class="mint-swipe-item">
          <img src="../../assets/asset/1.png" alt="" class="swipe_img1">
        </mt-swipe-item>
        <mt-swipe-item class="mint-swipe-item">
          <img src="../../assets/asset/2.png" alt="" class="swipe_img1">
        </mt-swipe-item>
        <mt-swipe-item class="mint-swipe-item">
          <img src="../../assets/asset/3.png" alt="" class="swipe_img1">
        </mt-swipe-item>
        <mt-swipe-item class="mint-swipe-item">
          <img src="../../assets/asset/4.png" alt="" class="swipe_img1">
        </mt-swipe-item>
        <mt-swipe-item class="mint-swipe-item">
          <img src="../../assets/asset/5.png" alt="" class="swipe_img1">
        </mt-swipe-item>
      </mt-swipe>
    </div>
      <!--轮播图结束  -->
       <!--内容分栏开始  -->
        <div class="third">
          <div class="thirds">
            <div class="divsa"></div>
            <h2> —— 附近商家 ——</h2>
          </div>
        </div>
       <!--内容分栏结束  -->

      <!-- 内容选项卡开始 -->
      <!-- 顶部开始 -->
      <div class="fixed">
        <mt-navbar v-model="active">
            <mt-tab-item id="a">综合排序</mt-tab-item>
            <mt-tab-item id="b">销量最高</mt-tab-item>
            <mt-tab-item id="c">距离最近</mt-tab-item>
            <mt-tab-item id="d">筛选</mt-tab-item>
        </mt-navbar>
      </div>
      <!-- 顶部结束 -->
      <!-- 面板开始 -->
      <mt-tab-container v-model="tab">
          <mt-tab-container-item id="china">
              <div v-for="(k,v) of 10" :key="v">
                <div class="infoItemContent">
                  <img class="infoItemImg" src="../../assets/articles/2.png" alt=""  />
                  <div class="infoItemDes">
                    <span class="foura">麻辣香锅</span><br>
                    <span >月售 300</span>
                    <span class="fours"> 重庆互联网学校旁</span><br>
                    <span>营业时间：08:30-20:00</span>
                  </div>
                </div>
              </div>
          </mt-tab-container-item>
          <mt-tab-container-item id="world">
              
          </mt-tab-container-item>
          <mt-tab-container-item id="sports">
              
          </mt-tab-container-item>
          <mt-tab-container-item id="env">
              
          </mt-tab-container-item>
      </mt-tab-container>
      <!-- 面板结束 -->
      <!-- 内容选项卡结束 -->

      </div>
</template>
<style scoped>
.container{
  margin-top:40px;
}
.first{
    background: ghostwhite;
    height: 200px;
}
.second {
 position: relative;
 left: -40px;
 margin-top:-12px ;
}
.second ul li{
  list-style: none;
  float: left;
  text-align: center;
  margin-left: 24px;
  
}
.second ul li img{
  height: 50px;
  width: 55px;
}
.seconds {
 position: relative;
 left: -40px;
 margin-top:105px ;
}
.seconds ul li{
  list-style: none;
  float: left;
  text-align: center;
  margin-left: 18px;
  
}
.seconds ul li img{
  height: 50px;
  width: 55px;
}
.secondas{
  margin-top: 10px;
}
p{
  padding: 0;
  margin: 0;
  font-family: fantasy;
  color: rgb(172, 172, 172);
}
/* 附近商家 */
.third{
  width: 100%;
  height: 80px;
  background: ghostwhite;
}
.thirds{
  color: rgb(114, 113, 113);
  text-align: center;
}
.divsa{
height:1px;
border-bottom:1px solid ghostwhite;
overflow:hidden;
}
/*内容*/
.infoItemContent {
  display: flex;
  padding-top: 11px;
  align-items: center;
  width: 100%;
}
.infoItemImg {
  width: 112px;
  border-radius: 5px;
  background: #ccc;
  margin-right: 15px;
}
.infoItemDes {
  font-size: 15px;
  overflow: hidden;
  font-weight: 400;
  text-overflow: ellipsis;
  line-height: 21px;
  letter-spacing: normal;
  color: #444;
  margin: 4px 15px 4px 0;
  height: 95px;
}
img[lazy="loading"] {
  height: 75px;
}
.foura{
  font-size: 20px;
}
.fours{
  margin-left: 30px;

}
/*  轮播图*/
.mint-swipe{
  width: 90%;
  height: 150px;
  margin: 15px auto;
  margin-top: 190px;
}
.swipe_img1{
  width: 100%;
  height: 150px;
  border-radius: 20px;
}
</style>
<script>
export default {
  data(){
    return {
      active:'a',
      tab:'china',
      selected:'index'
    }
  },
  watch:{
      active(newValue){
        switch(newValue){
            case 'a':
              this.tab = 'china';
              break;
            case 'b':
              this.tab = 'world';
              break;
            case 'c':
              this.tab = 'sports';
              break;
            case 'd':
              this.tab = 'env';
              break;
        }
      },
  },
}
</script>
