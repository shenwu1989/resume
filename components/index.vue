<template>
  <div class="index">
    <!--头-->
    <div class="index-top">
      <a href="#">
        <img src="../../static/img/128.png" alt="">
      </a>
      <div>
        <span>阴阳师</span>
        <p>网易和风匠心巨制</p>
      </div>
      <a href="#"></a>
    </div>
    <div class="index-center">
      <div class="index-one">
        <div class="banner">
          <a href="#">
            <img src="../../static/img/banner_11134e9.jpg" alt="">
          </a>
        </div>
        <a href="#"></a>
      </div>
      <!--资料片-->
      <div class="index-yuyue">
        <h3>新区集结 预约豪礼</h3>
        <i><i></i></i>
        <ul>
          <li>
            <i class="lb-1"></i>
            <em>祝福礼包</em>
            <span>100,000</span>
          </li>
          <li>
            <i class="lb-2"></i>
            <em>皮肤礼包</em>
            <span>300,000</span>
          </li>
          <li>
            <i class="lb-3"></i>
            <em>勾玉礼包</em>
            <span>500,000</span>
          </li>
          <li>
            <i class="lb-4"></i>
            <em>神秘符咒</em>
            <span>800,000</span>
          </li>
          <li>
            <i class="lb-5"></i>
            <em>月见之樱</em>
            <span>1000,000</span>
          </li>
        </ul>
        <p class="index-p1">
          <i></i>
          <span>《枫之舞》将于11月7日10:00开启</span>
          <i></i>
        </p>
        <a href="#"></a>
        <p class="index-p2">已预约<span>3110462</span></p>
      </div>
      <!--新闻咨询-->
      <div class="index-xwzx">
        <h2 class="top-img"><img src="../../static/img/tit1_3d78f4c.png" alt=""></h2>
        <div>
          <ul>
            <li v-for="(i,index) in xwliList" :key="index">
              <div v-for="(a,b) in i.xwdivList" :key="b">
              <a href="#">
                <span v-text="a.title"></span>
                <p v-text="a.content"></p>
                <em></em>
              </a>
            </div>
            </li>

          </ul>
          <a href="javascript:;" class="prev_news">上一页</a>
          <a href="javascript:;" class="next_news">下一页</a>
          <span></span>
          <a href="#" class="more_news">更多</a>
        </div>
      </div>
      <!-- 阴阳师手账 -->
      <div class="index-yyssz">
        <h2 class="top-img">
          <img src="../../static/img/tit2_0c9e302.png" alt="">
        </h2>
        <div>
          <ul>
            <li v-for="(i,index) in szliList" :key="index">
              <a href="#">
                <span>
                  <img :src="i.url" alt="">
                </span>
                <b v-text="i.title"></b>
              </a>
            </li>
          </ul>
        </div>
      </div>
      <!--平安世界-->
      <div class="index-pasj">
        <h2 class="top-img">
          <img src="../../static/img/tit3_6dd14e4.png" alt="">
        </h2>
        <p>
          <a href="#" class="on">式神录</a>
          <a href="#" >主角录</a>
          <a href="#" >声优阵</a>
        </p>
       <!-- 式神录-->
        <div class="index-pasj-ssl show">
          <div class="ssl-nav">
            <a href="javascript:;" class="on" @click="quan($event)">全部</a>
            <a href="javascript:;" @click="liandong($event)">联动</a>
            <a href="javascript:;" @click="SP($event)">SP</a>
            <a href="javascript:;" >SSR</a>
            <a href="javascript:;" >SR</a>
            <a href="javascript:;" >R</a>
            <a href="javascript:;">N</a>
            <a href="javascript:;" >呱太</a>
          </div>
          <ul class="ssl-img">
            <li v-for="(i,index) in sslList" :key="index" :alt="index" >
              <a  :href="'#?id='+a.id" v-for="(a,eq) in i.sslImgList" :key="eq">
                <img :src='"../../static/img/"+a.url' alt="">
                <p v-text="a.name"></p>
                <em :class="a.id<=3?'show':'hide'"></em>
              </a>
            </li>
          </ul>
          <ol class="ssl-button">
            <li v-for="(i,index) in sslList" :key="index" ></li>
          </ol>
        </div>
       <!-- 猪脚录-->
        <div class="index-pasj-zjl">
          <div class="zjl-nav">
            <a href="javascript:;" class="on">晴明 <em></em></a>
            <a href="javascript:;">神乐 <em></em></a>
            <a href="javascript:;">源博雅 <em></em></a>
            <a href="javascript:;">八百比丘尼 <em></em></a>
          </div>
          <ul class="zjl-swiper">
            <li>
              <div>
                <img src="../../static/img/1_n_419d8f1.png" alt="">
                <a href="javascript:;"></a>
                <em></em>
              </div>
              <p></p>
              <em></em>
            </li>
            <li>
              <div>
                <img src="../../static/img/2_n_614412f.png" alt="">
                <a href="javascript:;"></a>
                <em></em>
              </div>
              <p></p>
              <em></em>
            </li>
            <li>
              <div>
                <img src="../../static/img/3_n_24678bc.png" alt="">
                <a href="javascript:;"></a>
                <em></em>
              </div>
              <p></p>
              <em></em>
            </li>
            <li>
              <div>
                <img src="../../static/img/4_n_bd0649e.png" alt="">
                <a href="javascript:;"></a>
                <em></em>
              </div>
              <p></p>
              <em></em>
            </li>
          </ul>
          <a href="javascript:;" class="prev">
            <p>
              <i></i>
              <span>八百比丘尼</span>
            </p>
            <span></span>
          </a>
          <a href="javascript:;" class="next">
            <p>
              <i></i>
              <span>神乐</span>
            </p>
            <span></span>
          </a>
          <a href="#" class="more">了解更多</a>
        </div>
        <!--声优阵-->
       <div class="index-pasj-ssz">
         <ul>
           <li>安部壮一</li>
           <li>户松遥</li>
           <li>日高里菜</li>
           <li>梶裕贵</li>
           <li>安元洋贵</li>
           <li>花江夏树</li>
           <li>三森铃子</li>
           <li>西谷修一</li>
           <li>白石凉子</li>
           <li>花泽香菜</li>
           <li>桑岛法子</li>
           <li>喜多村英梨</li>
           <li>阪口周平</li>
           <li>吉野裕行</li>
           <li>森久保祥太郎</li>
           <li>细谷佳正</li>
           <li>保志总一朗</li>
           <li>加隈亚衣</li>
           <li>山口胜平</li>
           <li>小林大纪</li>
           <li>滨野大辉</li>
           <li>甲斐田裕子</li>
           <li>杉山纪彰</li>
           <li>小林优</li>
           <li>茶风林</li>
           <li>间宫康弘</li>
           <li>杉田智和</li>
           <li>小清水亚美</li>
           <li>成田剑</li>
           <li>近藤唯</li>
           <li>上坂堇</li>
           <li>小西克幸</li>
           <li>池田海咲</li>
           <li>井口裕香</li>
           <li>石川界人</li>
           <li>小野坂昌也</li>
           <li>川澄绫子</li>
           <li>井上和彦</li>
           <li>石田彰</li>
           <li>新谷真弓</li>
           <li>寸石和弘</li>
           <li>井上麻里奈</li>
           <li>柿原彻也</li>
           <li>岩崎了</li>
           <li>佐藤聪美</li>
           <li>井泽诗织</li>
           <li>水濑祈</li>
           <li>伊藤静</li>
           <li>大泊贵挥</li>
           <li>君岛哲</li>
           <li>水树奈奈</li>
           <li>樱井透</li>
           <li>大原沙耶香</li>
           <li>堀江由衣</li>
           <li>松冈祯丞</li>
           <li>樱井孝宏</li>
           <li>代永翼</li>
           <li>立花慎之介</li>
           <li>松井晓波</li>
           <li>悠木碧</li>
           <li>岛崎信长</li>
           <li>铃村健一</li>
           <li>松田健一郎</li>
           <li>由加奈</li>
           <li>钉宫理惠</li>
           <li>铃木达央</li>
           <li>田村由香里</li>
           <li>有贺由树子</li>
           <li>渡边优里奈</li>
           <li>绿川光</li>
           <li>梶裕贵</li>
           <li>羽饲真梨</li>
           <li>丰崎爱生</li>
           <li>茅野爱衣</li>
           <li>西谷修一</li>
           <li>远藤大辅</li>
           <li>福山润</li>
           <li>名冢佳织</li>
           <li>喜多村英梨</li>
           <li>早见沙织</li>
           <li>高山南</li>
           <li>内田真礼</li>
           <li>细谷佳正</li>
           <li>泽城美雪</li>
           <li>弓原健史</li>
           <li>能登麻美子</li>
           <li>小林大纪</li>
           <li>增田俊树</li>
           <li>宮本誉之</li>
           <li>鸟海浩辅</li>
           <li>小林优</li>
           <li>斋藤千和</li>
           <li>关俊彦</li>
           <li>平川大辅</li>
           <li>小清水亚美</li>
           <li>中村悠一</li>
           <li>行成桃姬</li>
           <li>朴璐美</li>
           <li>小西克幸</li>
           <li>中井和哉</li>
           <li>河西健吾</li>
           <li>前野智昭</li>
           <li>小野坂昌也</li>
           <li>种崎敦美</li>
         </ul>
       </div>
      </div>
      <!--游戏攻略-->
      <div class="index-yxgl">
        <h2 class="top-img">
          <img src="../../static/img/tit4_8cbf2d1.png" alt="">
        </h2>
        <span></span>
        <div class="yxgl-img">
          <a href="#">
            <img src="../../static/img/1f76aa4d-f471-4a04-90e2-aa4aed3c2c40.jpg" alt="">
            <p>妖气副本-悬赏封印</p>
          </a>
          <a href="#">
            <img src="../../static/img/70eea6cd-65c8-47b9-b2bb-e0502976ce8e.jpg" alt="">
            <p>浮梦花烛-秘闻副本</p>
          </a>
          <a href="#">
            <img src="../../static/img/4e450acd-3427-40ba-897f-d5c3345fc78b.jpg" alt="">
            <p>逢魔进阶-蜃气楼</p>
          </a>
        </div>
        <ol>
          <li class="on">萌新上路</li>
          <li>式神御魂</li>
          <li>秘闻副本</li>
          <li>斗技阵容</li>
        </ol>
        <div class="yxgl-swiper">
          <ul>
            <li v-for="(i,index) in yxglList" :key="index">
              <div v-for="(a,eq) in i.List" :key="eq">
                <a :href="'#?id='+a.id">
                  <p v-text="a.title"></p>
                  <span v-text="a.name"></span>
                </a>
              </div>
            </li>
          </ul>
        </div>
        
      </div>
     <!-- 同人收账-->
      <div class="index-trsz">
        <h2 class="top-img">
          <img src="../../static/img/tit5_3f5971b.png" alt="">
        </h2>
        <em></em>
        <!--热门活动-->
        <div class="trsz-rmhd">
          <h3>热门活动</h3>
          <ol>
            <li class="on"></li>
            <li></li>
            <li></li>
          </ol>
        </div>
        <div class="rmhd-swiper">
          <ul>
            <li>
              <a href="" >
                <img src="../../static/img/b64bab0b-58c3-4509-b713-8e895bf20613.jpg" alt="">
              </a>
            </li>
            <li>
              <a href="" >
                <img src="../../static/img/a938dc51-119e-4c69-9b87-9a018c0d8db9.png" alt="">
              </a>
            </li>
            <li>
              <a href="" >
                <img src="../../static/img/77e6749f-97bb-4474-8215-866bf6055310.png" alt="">
              </a>
            </li>
          </ul>
        </div>
        <!--热门作品-->
        <div class="trsz-rmzp">
          <h3>热门作品</h3>
        </div>
        <div class="rmzp-swiper">
          <ul>
            <li v-for="(i,index) in rmzpList" :key="index">
              <a :href="'#?id='+i.id">
                <img :src="src+i.url" alt="">
                <p>
                  <b v-text="i.title"></b>
                  <span v-text="i.name"></span>
                </p>
              </a>
              <span v-text="i.num"></span>
            </li>
          </ul>
        </div>
        <div class="arrow">
          <a href="javascript:;"></a>
          <a href="javascript:;"></a>
        </div>
        <!--同人大触-->
        <div class="trdc-top">
          <h3>同人大触</h3>
          <a href="#">阴阳师同人手帐</a>
        </div>
        <div class="trdc-swiper">
          <ul>
            <li v-for="(i,index) in trdcList" :key="index">
              <a :href="'#?id='+i.id">
                <span>
                  <em v-text="i.title"></em>
                </span>
                <p>
                  <img :src="src+i.url" alt="">
                </p>
              </a>
            </li>
          </ul>
        </div>
        <div class="arrow">
          <a href="javascript:;"></a>
          <a href="javascript:;"></a>
        </div>
      </div>
      <!--泛娱乐-->
      <div class="index-fyl">
        <h2 class="top-img"><img src="../../static/img/tit6_49791a4.png" alt=""></h2>
        <em></em>
        <div>
          <ul>
            <li>
              <a href="#">
                <img src="../../static/img/4dd0bdbf-970d-4753-a768-34f7ff8f81cc.gif" alt="">
              </a>
            </li>
            <li>
              <a href="">
                <img src="../../static/img/bff0e2c8-b425-4611-8e42-d6d47e6ccab8.png" alt="">
              </a>
            </li>
            <li>
              <a href="">
                <img src="../../static/img/2964b235-2da9-4e9f-9218-b46bcd9f999a.png" alt="">
              </a>
            </li>
            <li>
              <a href="#">
                <img src="../../static/img/bccac189-b024-4476-8969-266aaa9d2891.png" alt="">
              </a>
            </li>
            <li>
              <a href="">
                <img src="../../static/img/b5f6f875-b5f4-42b9-89a7-3024388c4d17.png" alt="">
              </a>
            </li>
            <li>
              <a href="">
                <img src="../../static/img/ab70e640-c20b-4c59-b1c7-d9759206e2ce.png" alt="">
              </a>
            </li>
          </ul>
          <a href="javascript:;" class="prev_fyl"></a>
          <a href="javascript:;" class="next_fyl"></a>
        </div>
      </div>
      <!--京都商业街-->
      <div class="index-jdsyj">
        <h2 class="top-img"><img src="../../static/img/tit7_6de0e50.png" alt=""></h2>
      </div>
    </div>
   
  </div>
</template>

<script>
  export default {
    data(){
      return{
        xwliList:[
          {
            xwdivList:[
              {
                title:'福利情报曝光！网易游戏三种会员模式全面开启',
                content:'网易游戏会员俱乐部三种会员模式已全面开启！“网易游戏会员”、“网易游戏超级会员年卡”、“网易大会员年卡”，提供多样福利，全方位……',
                id:'1'
              },
              {
                title:'集结召唤开启！《阴阳师》SP炼狱茨木童子降临',
                content:'黯淡的天际，月色微微而现，山林之间却如水般平静。山径之上，坚实有力的脚步声传来，从荒山前来的炼狱茨木童子身影缓缓出现，终于来到……',
                id:2
              },
              {
                title:'《阴阳师》手游11月7日维护更新公告',
                content:'亲爱的阴阳师大人：为了给大家带来更好的游戏体验，服务器将于11月7日（周三）早上6:30-9:00进行停服维护，如未能按时完成，则开服时间将会顺延。具体更新详情请留意稍后更新公告，或维护结束后至游戏登录界面查看。',
                id:3
              },
              {
                title:'急急如律令！《阴阳师》晴明黏土手办登场！',
                content:'飘雪的初冬，繁星点点，月色给雪地铺上了一纱流光。与往日不同，周边屋前萦绕着阵阵笑语：“晴明，我们走快点……”少女身穿绯红和服……',
                id:4
              },
              {
                title:'来自前辈的守护 《阴阳师》羁绊预约开启！',
                content:'初入平安京时，看不懂的御魂搭配，不熟悉的式神和多样复杂的阵容套路，总让人摸不着头脑~面对着残暴的麒麟和凶狠的八岐大蛇，初至平安……',
                id:5
              },
              {
                title:'长刀舞 战风起《阴阳师》妖刀姬新装登场！',
                content:'烽火烈烈，四起的狼烟中是厮杀的呼号，飞驰的利箭如瓢泼大雨般落下，遍野哀声中，箭矢折断的声音与刀鸣相织。鲜血飞溅，破空而过的长刀……',
                id:6
              }
            ]
          },
          {
            xwdivList:[
              {
                title:'福利情报曝光！网易游戏三种会员模式全面开启',
                content:'网易游戏会员俱乐部三种会员模式已全面开启！“网易游戏会员”、“网易游戏超级会员年卡”、“网易大会员年卡”，提供多样福利，全方位……',
                id:'1'
              },
              {
                title:'福利情报曝光！网易游戏三种会员模式全面开启',
                content:'网易游戏会员俱乐部三种会员模式已全面开启！“网易游戏会员”、“网易游戏超级会员年卡”、“网易大会员年卡”，提供多样福利，全方位……',
                id:2
              },
              {
                title:'福利情报曝光！网易游戏三种会员模式全面开启',
                content:'网易游戏会员俱乐部三种会员模式已全面开启！“网易游戏会员”、“网易游戏超级会员年卡”、“网易大会员年卡”，提供多样福利，全方位……',
                id:3
              },
              {
                title:'福利情报曝光！网易游戏三种会员模式全面开启',
                content:'网易游戏会员俱乐部三种会员模式已全面开启！“网易游戏会员”、“网易游戏超级会员年卡”、“网易大会员年卡”，提供多样福利，全方位……',
                id:4
              },
              {
                title:'福利情报曝光！网易游戏三种会员模式全面开启',
                content:'网易游戏会员俱乐部三种会员模式已全面开启！“网易游戏会员”、“网易游戏超级会员年卡”、“网易大会员年卡”，提供多样福利，全方位……',
                id:5
              },
              {
                title:'福利情报曝光！网易游戏三种会员模式全面开启',
                content:'网易游戏会员俱乐部三种会员模式已全面开启！“网易游戏会员”、“网易游戏超级会员年卡”、“网易大会员年卡”，提供多样福利，全方位……',
                id:6
              }
            ]
          },
          {
            xwdivList:[
              {
                title:'福利情报曝光！网易游戏三种会员模式全面开启',
                content:'网易游戏会员俱乐部三种会员模式已全面开启！“网易游戏会员”、“网易游戏超级会员年卡”、“网易大会员年卡”，提供多样福利，全方位……',
                id:'1'
              },
              {
                title:'福利情报曝光！网易游戏三种会员模式全面开启',
                content:'网易游戏会员俱乐部三种会员模式已全面开启！“网易游戏会员”、“网易游戏超级会员年卡”、“网易大会员年卡”，提供多样福利，全方位……',
                id:2
              },
              {
                title:'福利情报曝光！网易游戏三种会员模式全面开启',
                content:'网易游戏会员俱乐部三种会员模式已全面开启！“网易游戏会员”、“网易游戏超级会员年卡”、“网易大会员年卡”，提供多样福利，全方位……',
                id:3
              },
              {
                title:'福利情报曝光！网易游戏三种会员模式全面开启',
                content:'网易游戏会员俱乐部三种会员模式已全面开启！“网易游戏会员”、“网易游戏超级会员年卡”、“网易大会员年卡”，提供多样福利，全方位……',
                id:4
              },
              {
                title:'福利情报曝光！网易游戏三种会员模式全面开启',
                content:'网易游戏会员俱乐部三种会员模式已全面开启！“网易游戏会员”、“网易游戏超级会员年卡”、“网易大会员年卡”，提供多样福利，全方位……',
                id:5
              },
              {
                title:'福利情报曝光！网易游戏三种会员模式全面开启',
                content:'网易游戏会员俱乐部三种会员模式已全面开启！“网易游戏会员”、“网易游戏超级会员年卡”、“网易大会员年卡”，提供多样福利，全方位……',
                id:6
              }
            ]
          }
        ],
        szliList:[
          {url:'../../static/img/rl5_c64607d.png',title:'主角录'},
          {url:'../../static/img/rl7_e988aca.png',title:'同人赏'},
          {url:'../../static/img/rl9_386baba.png',title:'同人文'},
          {url:'../../static/img/rl10_4e5bdf7.png',title:'游戏特色'},
          {url:'../../static/img/rl11_a8d9f35.png',title:'大事记'},
          {url:'../../static/img/rl12_14f30b3.png',title:'开服计划'},
          {url:'../../static/img/rl13_a539a99.png',title:'悬赏封印'},
          {url:'../../static/img/rl1_dfed6f1.png',title:'游戏日历'},
          {url:'../../static/img/rl2_8542a23.png',title:'微博活动'},
          {url:'../../static/img/rl3_f1318fb.png',title:'微信活动'},
          {url:'../../static/img/rl4_b4459c9.png',title:'论坛活动'},
        ],
        sslList:[
          {
            sslImgList:[
              {name:'一反木绵',url:'320.jpg',id:'1'},
              {name:'入殓师',url:'321.jpg',id:'2'},
              {name:'炼狱茨木童子',url:'322.jpg',id:'3'},
              {name:'於菊虫',url:'318.jpg',id:'4'},
              {name:'桔梗',url:'319.jpg',id:'5'},
              {name:'人面树',url:'317.jpg',id:'6'},
              {name:'白藏主',url:'316.jpg',id:'7'},
              {name:'少羽大天狗',url:'315.jpg',id:'8'},
              {name:'鬼切',url:'312.jpg',id:'9'},
              {name:'杀生丸',url:'314.jpg',id:'10'},
              {name:'犬夜叉',url:'313.jpg',id:'11'},
              {name:'彼岸花呱',url:'427.jpg',id:'12'},
              {name:'荒呱',url:'426.jpg',id:'13'},
              {name:'辉夜姬呱',url:'425.jpg',id:'14'},
              {name:'花鸟卷呱',url:'424.jpg',id:'15'},
            ]
          },
          {
            sslImgList:[
              {name:'一目连呱',url:'423.jpg',id:'16'},
              {name:'妖刀姬呱',url:'422.jpg',id:'17'},
              {name:'青行灯呱',url:'421.jpg',id:'18'},
              {name:'茨木呱',url:'420.jpg',id:'19'},
              {name:'小鹿男呱',url:'419.jpg',id:'20'},
              {name:'两面佛呱',url:'418.jpg',id:'21'},
              {name:'阎魔呱',url:'417.jpg',id:'22'},
              {name:'荒川呱',url:'416.jpg',id:'23'},
              {name:'酒吞呱',url:'415.jpg',id:'24'},
              {name:'大天狗呱',url:'414.jpg',id:'25'},
              {name:'面灵气',url:'311.jpg',id:'26'},
              {name:'猫掌柜',url:'307.jpg',id:'27'},
              {name:'蜜桃&芥子',url:'310.jpg',id:'28'},
              {name:'阿香',url:'309.jpg',id:'29'},
              {name:'鬼灯',url:'308.jpg',id:'30'},
            ]
          },
        ],
        sllLeft:0,
        yxglList:[
          {
            List:[
              {title:'【新手】第四期！ 御魂从哪来？躺魂十的各种姿势！',name:"作者：Yeno1996",id:'1'},
              {title:'【新手】第四期！ 御魂从哪来？躺魂十的各种姿势！',name:'作者：Yeno1996',id:'2'},
              {title:'【新手】第三期 你们应该强化的御魂是这样滴~',name:'作者：Yeno1996',id:'3'},
            ]
          },
          {
            List:[
              {title:'【式神】防御机制与人面树测试报告',name:"作者：木子南",id:'4'},
              {title:'【式神】白藏主机制及正确使用指南',name:'作者：木子南',id:"5"},
              {title:'【式神】阴阳天机谱 | 幼羽缠风，崇天无畏山高远',name:'作者：鸽海成路',id:'6'},
            ]
          },
          {
            List:[
              {title:'【玩法】新人的地狱鬼王攻略',name:"作者：木子南",id:'7'},
              {title:'【玩法】休闲玩家进阶之夺得荒骷髅最高成就',name:'作者：西城男孩',id:"8"},
              {title:'【玩法】周年庆视觉更新！活动先览！（20180912体服速报）',name:'作者：小武哥',id:"9"},
            ]
          },
          {
            List:[
              {title:'【斗技】【翻牌攻略】斗技先手流（上篇）',name:"作者：木子南",id:'10'},
              {title:'【斗技】为崽而战课堂：大佬来看看这里有没有你常用的斗技阵容',name:'作者：Yeno1996',id:"11"},
              {title:'【斗技】为崽而战小课堂：兵俑雪女凤凰火，那个是神级控？',name:'作者：Yeno1996',id:'12'},
            ]
          }
        ],
        src:'../../static/img/',
        rmzpList:[
          {url:"063b122b-e651-47c2-8988-5e114144c934.jpg",title:'COS：烟烟罗',name:'作者：桃沢西凉',num:'263',id:'1'},
          {url:"230fbe70-db2a-4df9-9c5c-3ebeb0bece4a.jpg",title:'COS：鬼使黑',name:'作者：相知大总攻Lewis',num:'283',id:'2'},
          {url:"53aab520-17cf-4ec9-bfd9-1a3253cc5ddf.jpg",title:'COS：鬼女红叶·觉醒',name:'作者：充斥盐酸',num:'271',id:'3'},
          {url:"206261fe-2ea3-4bd3-9c9c-3d36de8c585f.jpg",title:'彼岸花×荒骷髅',name:'作者：椿煊',num:'227',id:'4'},
          {url:"4f97beed-be1d-4573-b2a9-073a583588f6.jpg",title:'COS：玉藻前×巫女',name:'作者：寒少末&小懒宝贝',num:'283',id:'5'},
          {url:"45c452db-7412-455c-b330-1dea1b3600e6.jpg",title:'COS：吸血姬，让我吸一口血',name:'作者：墨瑜酱',num:'258',id:'6'},
          {url:"00ed2ea4-133e-4d98-9d75-7fdbc47f23f8.jpg",title:'手作：一目连，堕妖也不忘守护',name:'作者：5坦夫斯基',num:'249',id:'7'},
          {url:"f76e9444-06ba-4df2-a7db-37f57ceaa647.jpg",title:'山有尽时，少年亭亭如盖',name:'作者：夜城先森',num:'225',id:'8'},
          {url:"765fabb6-814f-463f-af45-821ee7e478e4.jpg",title:'小鹿男是美少年',name:'作者：燃尽水域',num:'241',id:'9'}
        ],
        trdcList:[
          {url:'d8bdbbba-78bc-4f57-9d0b-e6e368d54e13.jpg',title:'5坦夫斯基',id:'1'},
          {url:'903591c4-29cb-4188-b408-205894c64464.jpg',title:'第五橙-',id:'2'},
          {url:'6493f6f4-0bf5-4571-9f14-2b921a39b701.jpg',title:'会飞的荷子',id:'3'},
          {url:'eacf370e-053b-4b30-a651-cc11ced75b4d.png',title:'渡渔',id:'4'},
          {url:'264146d7-7452-4867-b41f-ba5e972d0266.jpg',title:'一条青虫-',id:'5'},
          {url:'e8bad0f2-25f3-45c8-8d59-767927db489a.jpg',title:'与月MOON',id:'6'},
          {url:'b52b96c4-fa59-48bb-841c-cd87ddc7c929.jpg',title:'白白努力肝图中',id:'7'},
          {url:'f2cb5f60-ae49-4b31-9bc4-7cc2dbc5d3a3.jpg',title:'Aque榊淚',id:'8'},
          {url:'33250df7-91e2-44e5-8e56-65883a1fdf93.jpg',title:'考拉',id:'9'},
          {url:'3b6fe866-584b-4b39-8717-47ec246a3d2e.jpg',title:'MR_PLEIADES',id:'10'},
          {url:'bfb4f657-2c32-43b6-a783-e74560d340b6.jpg',title:'KAKYUU',id:'11'},
          {url:'f0e1bc6f-89c6-4f3b-92ff-4e0c9cd3d239.jpg',title:'昊的黏答答地狱',id:'12'}
        ]
      }
    },
    methods:{
      quan(e){//全部图片模拟
        this.sslList=[
          {
            sslImgList:[
              {name:'一反木绵',url:'320.jpg',id:'1'},
              {name:'入殓师',url:'321.jpg',id:'2'},
              {name:'炼狱茨木童子',url:'322.jpg',id:'3'},
              {name:'於菊虫',url:'318.jpg',id:'4'},
              {name:'桔梗',url:'319.jpg',id:'5'},
              {name:'人面树',url:'317.jpg',id:'6'},
              {name:'白藏主',url:'316.jpg',id:'7'},
              {name:'少羽大天狗',url:'315.jpg',id:'8'},
              {name:'鬼切',url:'312.jpg',id:'9'},
              {name:'杀生丸',url:'314.jpg',id:'10'},
              {name:'犬夜叉',url:'313.jpg',id:'11'},
              {name:'彼岸花呱',url:'427.jpg',id:'12'},
              {name:'荒呱',url:'426.jpg',id:'13'},
              {name:'辉夜姬呱',url:'425.jpg',id:'14'},
              {name:'花鸟卷呱',url:'424.jpg',id:'15'},
            ]
          },
          {
            sslImgList:[
              {name:'一目连呱',url:'423.jpg',id:'16'},
              {name:'妖刀姬呱',url:'422.jpg',id:'17'},
              {name:'青行灯呱',url:'421.jpg',id:'18'},
              {name:'茨木呱',url:'420.jpg',id:'19'},
              {name:'小鹿男呱',url:'419.jpg',id:'20'},
              {name:'两面佛呱',url:'418.jpg',id:'21'},
              {name:'阎魔呱',url:'417.jpg',id:'22'},
              {name:'荒川呱',url:'416.jpg',id:'23'},
              {name:'酒吞呱',url:'415.jpg',id:'24'},
              {name:'大天狗呱',url:'414.jpg',id:'25'},
              {name:'面灵气',url:'311.jpg',id:'26'},
              {name:'猫掌柜',url:'307.jpg',id:'27'},
              {name:'蜜桃&芥子',url:'310.jpg',id:'28'},
              {name:'阿香',url:'309.jpg',id:'29'},
              {name:'鬼灯',url:'308.jpg',id:'30'},
            ]
          },
        ];
        this.sslNavOn(e);
      },
      liandong(e){//联动图片模拟
        this.sslList=[{
          sslImgList:[
            {name:'鬼切',url:'312.jpg',id:'9'},
            {name:'杀生丸',url:'314.jpg',id:'10'},
            {name:'犬夜叉',url:'313.jpg',id:'11'},
            {name:'彼岸花呱',url:'427.jpg',id:'12'},
            {name:'荒呱',url:'426.jpg',id:'13'},
            {name:'辉夜姬呱',url:'425.jpg',id:'14'},
            {name:'花鸟卷呱',url:'424.jpg',id:'15'},
          ]
        }];
        this.sslNavOn(e);
      },
      SP(e){//sp
        this.sslList=[{
          sslImgList:[
            {name:'炼狱茨木童子',url:'322.jpg',id:'3'},
            {name:'少羽大天狗',url:'315.jpg',id:'8'},
          ]
        }];
        this.sslNavOn(e);
      },
      SSR(){

      },
      sslNavOn(e){//ssl-nav添加on事件
       for(var i=0;i<e.target.parentNode.children.length;i++){
         e.target.parentNode.children[i].classList.remove('on');
       };
        e.target.setAttribute('class','on');
      },
      sslBtn(){//ssl-button按钮选中事件
        var ul = document.querySelector('ul.ssl-img');
        var dName= document.querySelector('div.index-pasj-ssl');
        var display = window.getComputedStyle(dName,null).getPropertyValue("display");
        if(display !='none'){
          var w = ul.offsetWidth;
          this.sllLeft = ul.offsetLeft;
          var eq = Math.abs(this.sllLeft/w);
          var ol = document.querySelector('ol.ssl-button');
          ol.children[eq].classList.add('on');
        }
      }
    },
    created(){
      //console.log(this.xwliList)
    },//渲染前执行
    mounted(){
      this.sslBtn()
    }//渲染后执行
  }
  

</script>

<style scoped>

</style>
