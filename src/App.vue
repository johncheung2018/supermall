<template>
  <div id="app">
  <router-view></router-view>
      <tab-bar>
        <tab-bar-item path="/home">
            <img slot="item-icon" src='./assets/img/tabbar/1.png'>
            <img slot="item-icon-active" src='./assets/img/tabbar/11.png'>
            <div slot="item-text">首页</div>
        </tab-bar-item>
        <tab-bar-item path="/category">
            <img slot="item-icon" src='./assets/img/tabbar/2.png'>
            <img slot="item-icon-active" src='./assets/img/tabbar/22.png'>
            <div slot="item-text">分类</div>
        </tab-bar-item>
        <tab-bar-item path="/cart">
            <img slot="item-icon" src='./assets/img/tabbar/3.png'>
            <img slot="item-icon-active" src='./assets/img/tabbar/33.png'>
            <div slot="item-text">购物车</div>
        </tab-bar-item>
        <tab-bar-item path="/profile">
            <img slot="item-icon" src='./assets/img/tabbar/4.png'>
            <img slot="item-icon-active" src='./assets/img/tabbar/44.png'>
            <div slot="item-text">我的</div>
        </tab-bar-item>
      </tab-bar>
      
  </div>
</template>

<script>
import TabBar from './components/TabBar.vue'
import TabBarItem from './components/TabBarItem.vue'
export default {
  name: 'App',
  components:{
    TabBar,
    TabBarItem
  }
}
</script>

<style>
.tab-bar{display:flex;position:fixed;bottom:0;left: 0;right: 0;}
.tab-bar-item{flex:1;text-align:center;}
</style>
