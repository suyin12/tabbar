<template>
  <div id="app">
    <router-view></router-view>
    <main-tab-bar/>
  </div>
</template>

<script>

import MainTabBar from './components/MainTabBar'

export default {
  name: 'App',
  data() {
    return {

    }
  },
  components: {
    MainTabBar
  }
}
</script>
<!--vue 文件中可以用 @import 引入css文件-->
<style>
  @import "./assets/css/base.css";
</style>
