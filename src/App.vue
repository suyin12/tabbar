<template>
  <div id="app">
    <tab-bar>
      <tab-bar-item>
        <div slot="item-icon" v-if="!isActive"><img src="./assets/img/tabbar/home.svg" /></div>
        <div slot="item-icon" v-else><img src="./assets/img/tabbar/home_active.svg" /></div>
        <div slot="item-icon">首页</div>
      </tab-bar-item>
      <tab-bar-item>
        <div slot="item-icon" v-if="!isActive"><img src="./assets/img/tabbar/category.svg" /></div>
        <div slot="item-icon" v-else><img src="./assets/img/tabbar/category_active.svg" /></div>
        <div slot="item-icon">分类</div>
      </tab-bar-item>
      <tab-bar-item>
        <div slot="item-icon" v-if="!isActive"><img src="./assets/img/tabbar/shopcart.svg" /></div>
        <div slot="item-icon" v-else><img src="./assets/img/tabbar/shopcart_active.svg" /></div>
        <div slot="item-icon">购物车</div>
      </tab-bar-item>
      <tab-bar-item>
        <div slot="item-icon" v-if="!isActive"><img src="./assets/img/tabbar/profile.svg" /></div>
        <div slot="item-icon" v-else><img src="./assets/img/tabbar/profile_active.svg" /></div>
        <div slot="item-icon">我的</div>
      </tab-bar-item>
    </tab-bar>
  </div>
</template>

<script>
import TabBar from './components/tabbar/TabBar'
import TabBarItem from "./components/tabbar/TabBarItem";

export default {
  name: 'App',
  data() {
    return {
      isActive: true
    }
  },
  components: {
    TabBarItem,
    TabBar
  }
}
</script>
<!--vue 文件中可以用 @import 引入css文件-->
<style>
  @import "./assets/css/base.css";
</style>
