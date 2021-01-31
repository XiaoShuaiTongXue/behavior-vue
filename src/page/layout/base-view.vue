<template>
  <div class="wrapper">
    <div class="menu">
      <left-menu></left-menu>
    </div>
    <div class="main">
      <nav class="navbar navbar-expand navbar-light navbar-bg" style="z-index: 99999;position: fixed;width: 81%">
        <top-content></top-content>
      </nav>

      <!--嵌入页面-->
      <div class="content">
        <router-view></router-view>
      </div>

      <footer class="footer" style="bottom: 0;position: fixed;width: 81%">
        <bottom-content></bottom-content>
      </footer>
    </div>
  </div>
</template>
<script>
import LeftMenu from './left-menu'
import TopContent from './top-content'
import BottomContent from './bottom-content'
export default {
  components: {BottomContent, TopContent, LeftMenu}
}
</script>
<style>
@import "../../assets/css/app.css";
.wrapper{
  width: 100%;
}
.content{
  display: flex;
  flex-direction: column;
  height: 100%;
}
.menu{
  width: 300px;
}
</style>
