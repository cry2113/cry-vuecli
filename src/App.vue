<template>
  <div id="app" class="app-container">
    <mt-header fixed title="固定在顶部"></mt-header>
    <router-view></router-view>

    <mt-tabbar
      v-model="selected"
      class="tababr"
    >
      <mt-tab-item id="home">
        <router-link
          tag="span"
          to="/"
        >
          <i class="mui-icon mui-icon-home"></i> <br>
          主页</router-link>
      </mt-tab-item>
      <mt-tab-item id="member">
        <router-link
          tag="span"
          to="/member"
        >
          <i class="mui-icon mui-icon-contact"></i><br>
          会员</router-link>
      </mt-tab-item>
      <mt-tab-item id="cart" >
        <router-link
          tag="span"
          to="/cart"
        >
          <i class="mui-icon mui-icon-extra mui-icon-extra-cart">
            <i class="mui-badge">0</i>
          </i><br>
          购物车</router-link>
      </mt-tab-item>
      <mt-tab-item id="search">

        <router-link
          tag="span"
          to="/search"
        >
          <i class="mui-icon mui-icon-search"></i><br>
          搜索</router-link>
      </mt-tab-item>
    </mt-tabbar>
  </div>
</template>

<script>
export default {
  data(){
    return{
      selected:"home"
    }
  }
}
</script>


<style lang="less" scoped>
  .app-container {
    padding-top: 40px;
    padding-bottom: 55px;
    /*避免PC端网页在页面切换的时候出现的水平滚动条*/
    overflow: hidden;
  }
  .mui-icon-extra-cart{
    position: relative;
  }
  .mint-tab-item{
    color: grey;
  }
</style>
