<template>
  <div id="app">
    <a-layout id="components-layout-top" class="layout">
      <a-layout-header :style="{ background: '#fff' ,marginBottom:'1px',width:'100%',height:'80px'}">
        <img class="logo" src="./assets/web-logo.png" style="width:120px;height:46px"/>
        <a-menu
          theme="light"
          mode="horizontal"
          :style="{ lineHeight: '80px' ,fontSize:'20px',display:'flex',justifyContent:'flex-end'}"
        >
          <a-menu-item key="1">首页</a-menu-item>
          <a-menu-item key="2">产品</a-menu-item>
          <a-menu-item key="3">解决方案</a-menu-item>
          <a-menu-item key="3">联系我们</a-menu-item>
        </a-menu>

      </a-layout-header>

      <a-layout-content style=" width:100%">
        <router-view />
        <!-- <div :style="{ background: '#fff', padding: '24px', minHeight: '280px' }"><router-view/></div> -->
      </a-layout-content>

      <a-layout-footer style="text-align: center">Ant Design ©2018 Created by Ant UED</a-layout-footer>
    </a-layout>

    <!-- <div id="layout-fixed">

      <div class="layout-fixed-header">header</div>

      <div class="layout-fixed-content">content</div>

      <div class="layout-fixed-footer">footer</div>
    </div>-->
  </div>
</template>

<script>
export default {
  name: "App"
};
</script>

<style scoped>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin: 0 0 0 0;
  padding: 0 0;
  background: white;
}

#components-layout-top {
  /* background: white; */
 
  margin-left: 0;
  margin-top: 0px;
  width: 100%;
  height: 1000px;
}
#components-layout-top .logo {
  width: 120px;
  height: 36px;
  background: rgba(255, 255, 255, 0.2);
  margin: 16px 24px 16px 16px;
  float: left;

  background: red;
}


#components-layout-top .logo {
  width: 120px;
  height: 64px;
  background: rgba(255, 255, 255, 0.2);
  margin: 16px 24px 16px 0;
  float: left;
}


#layout-fixed {
  width: 100%;
  height: 100%;

  /* background: rgba(255,255,255,.2); */
  margin: 0px 0px 0px 0;
  background: red;
  /* float: left; */
}

#layout-fixed .layout-fixed-header {
  width: 100%;
  height: 80px;
  background: green;
}

#layout-fixed .layout-fixed-content {
  width: 100%;
  height: 80%;
  background: yellow;
}

#layout-fixed .layout-fixed-footer {
  width: 100%;
  height: 80%;
  background: black;
}

#components-layout-fixed .layout-header-menue {
  width: 100%;
  height: 80px;
}

#components-layout-fixed .logo {
  width: 120px;
  height: 31px;
  background: rgba(255, 255, 255, 0.2);
  margin: 16px 24px 16px 0;
  /* float: left; */
}
</style>
