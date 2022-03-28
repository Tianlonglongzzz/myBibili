<template>
  <div class="wrap">
    <div class="remen-box">
      <div class="txt-box">
        <span>热门推荐</span>
        <span class="paihang">
           <i class="iconfont biliicon-paixingbang"></i> 
           排行榜 
           <i class="iconfont biliicon-youjiantou"></i>
        </span>

      </div>
      <ul class="main-ul">
        <li v-for="(item, index) in arr1.tuijian" :key="index">
            <div class="li-box">
                <img :src="item.imgUrl" alt="">
                <p class="nums">
                    <span>
                        <i class="iconfont biliicon-danmushu"></i> {{item.bfnum}}
                    </span>
                    <span>
                       <i class="iconfont biliicon-shipinbofangliang"></i> {{item.plnum}}
                    </span>
                </p>
            </div>
          <p class="txt">{{ item.txt }}</p>
        </li>
      </ul>
    </div>
 <div class="remen-box">
      <div class="txt-box">
        <span>热门推荐</span>
        <span class="paihang">
           <i class="iconfont biliicon-paixingbang"></i> 
           排行榜 
           <i class="iconfont biliicon-youjiantou"></i>
        </span>

      </div>
      <ul class="main-ul">
        <li v-for="(item, index) in arr1.tuijian" :key="index">
            <div class="li-box">
                <img :src="item.imgUrl" alt="">
                <p class="nums">
                    <span>
                        <i class="iconfont biliicon-danmushu"></i> {{item.bfnum}}
                    </span>
                    <span>
                       <i class="iconfont biliicon-shipinbofangliang"></i> {{item.plnum}}
                    </span>
                </p>
            </div>
          <p class="txt">{{ item.txt }}</p>
        </li>
      </ul>
    </div> <div class="remen-box">
      <div class="txt-box">
        <span>热门推荐</span>
        <span class="paihang">
           <i class="iconfont biliicon-paixingbang"></i> 
           排行榜 
           <i class="iconfont biliicon-youjiantou"></i>
        </span>

      </div>
      <ul class="main-ul">
        <li v-for="(item, index) in arr1.tuijian" :key="index">
            <div class="li-box">
                <img :src="item.imgUrl" alt="">
                <p class="nums">
                    <span>
                        <i class="iconfont biliicon-danmushu"></i> {{item.bfnum}}
                    </span>
                    <span>
                       <i class="iconfont biliicon-shipinbofangliang"></i> {{item.plnum}}
                    </span>
                </p>
            </div>
          <p class="txt">{{ item.txt }}</p>
        </li>
      </ul>
    </div> <div class="remen-box">
      <div class="txt-box">
        <span>热门推荐</span>
        <span class="paihang">
           <i class="iconfont biliicon-paixingbang"></i> 
           排行榜 
           <i class="iconfont biliicon-youjiantou"></i>
        </span>

      </div>
      <ul class="main-ul">
        <li v-for="(item, index) in arr1.tuijian" :key="index">
            <div class="li-box">
                <img :src="item.imgUrl" alt="">
                <p class="nums">
                    <span>
                        <i class="iconfont biliicon-danmushu"></i> {{item.bfnum}}
                    </span>
                    <span>
                       <i class="iconfont biliicon-shipinbofangliang"></i> {{item.plnum}}
                    </span>
                </p>
            </div>
          <p class="txt">{{ item.txt }}</p>
        </li>
      </ul>
    </div>
  </div>
</template>
<style scoped>
    img{
        vertical-align: middle;
    }
    .txt{
        font-size: 12px;
        line-height: 20px;
        margin-bottom: 20px;
    }
    .li-box{
        position: relative;
        width: 100%;
    }
    .li-box .nums{
        padding: 0 10px;
        box-sizing: border-box;
        width: 100%;
        display: flex;
        justify-content: space-between;
        position: absolute;
        bottom: 0;
        left: 0;
        color: white;
        font-size: 13px;
        background:linear-gradient(0deg,rgba(0,0,0,.85),transparent);

    }

    .wrap{
        width: 100vw;
        height: 100vh;
    }
    .wrap .remen-box{
        width: 100%;
        margin-top: 10px;
    }
    .wrap .remen-box .txt-box{
        margin-bottom: 10px;
        display: flex;
        justify-content: space-between;
        flex-wrap: wrap;
        padding: 0 14px;
    }
    .paihang{
        color: orange;
    }
    ul,li{
        list-style: none;
    }
    img{
       width: 100%;
    }
    .main-ul{
        position: relative;
        margin-top: 15px;
        width: 100vw;
        display: flex;
        justify-content: space-around;
        flex-wrap: wrap;
    }
    .main-ul li{
        
       width: 45%;
    }
</style>
<script>
import instance from "../../api/index";
export default {
  name: "nav1",
  data() {
    return {
      arr1: null,
    };
  },
  methods: {
    async getTui() {
      let { data } = await instance.get("/music");
      console.log(data);
      this.arr1 = data;
    },
  },
  created() {
    this.getTui();
  },
};
</script>