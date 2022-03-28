<template>
  <div class="wrap">
    <nav class="nav-box">
      <router-link class="lis" active-class="act"  to="/nav1">推荐</router-link>
      <router-link class="lis" active-class="act"  to="/nav2">原创音乐</router-link>
      <router-link class="lis" active-class="act"  to="/nav3">翻唱</router-link>
      <router-link class="lis" active-class="act"  to="/nav4">VOCALOID-UTAU</router-link>
      <router-link class="lis" active-class="act"  to="/nav5">电音</router-link>
      <router-link class="lis" active-class="act"  to="/nav6">演奏</router-link>
      <router-link class="lis" active-class="act"  to="/nav7">MV</router-link>
      <router-link class="lis" active-class="act"  to="/nav8">音乐现场</router-link>
      <router-link class="lis" active-class="act"  to="/nav9">音乐综合</router-link>
    </nav>

    <div>
        <router-view />
    </div>
    
  </div>
</template>
<style scoped>
.act{
  color: deeppink;
  border-bottom: 2px solid deeppink;
}
  *{
    margin: 0;
    padding: 0;
  }
  a{
    text-decoration: none;
  }
  .nav-box{
    width: 100vw;
    height: 40px;
    overflow: scroll;
    font-size: 13px;
    justify-content: space-between;
    display: flex;
    border-bottom: 1px solid #ccc;
  }
  .nav-box::-webkit-scrollbar{
    display: none;
  }
  .nav-box .lis{
    padding: 0 10px;
    flex-shrink: 0;
    line-height: 40px;
  }
  
</style>
<script>
export default {
  name: "MyMusic",
};
</script>
