<template>
  <div id="app">
    <el-container>
      <el-header style="display:flex;justify-content:space-between;margin-top:12px;">
        <div class="menue-left header-height">
          <img src="./assets/web-logo.png" style="width:120px;" />
        </div>

        <div class="menue-right header-height">
          <el-menu
            :default-active="activeIndex"
            class="el-menu"
            mode="horizontal"
            @select="handleSelect"
          >
            <el-menu-item index="1"><span class="nav-font">首页</span></el-menu-item>
            <el-submenu index="2">
              <template slot="title"><span class="nav-font">产品</span></template>
               
              <el-menu-item index="2-1">产品1</el-menu-item>
              <el-menu-item index="2-2">产品2</el-menu-item>
              <el-menu-item index="2-3">产品3</el-menu-item>
            </el-submenu>
            <el-menu-item index="3"><span class="nav-font">解决方案</span></el-menu-item>
            <el-menu-item index="4">
              <a href="https://www.ele.me" target="_blank"><span class="nav-font">加入我们</span></a>
            </el-menu-item>

            <el-menu-item index="5"><span class="nav-font">搜索</span></el-menu-item>
            <el-menu-item index="6"><span class="nav-font"></span></el-menu-item>
            <el-menu-item index="7"><span class="nav-font"></span></el-menu-item>
          </el-menu>
          <div class="line"></div>
        </div>
      </el-header>
      <el-main style="width=100%;"><router-view/></el-main>

      <el-footer style="background:#303133;height:auto">
        <div style="padding-top:20px">
          <div style="display:flex;justify-content:center;">
            <div style="width:20%">
              <div>
                <span class="footer-title-font">科远通讯</span>
              </div>
              <div>
                <img style="width:120px;height:160px" src="./assets/foot-keyuan-book.png" />
              </div>
              <div>
                <span class="footer-content-font">《企业通讯录》</span>
              </div>
            </div>
            <div style="width:50%;display:flex;justify-content:space-around;">
              <div>
                <div>
                  <span class="footer-title-font">支持与服务</span>
                </div>

                <div>
                  <el-link href="https://element.eleme.io" target="_blank">
                    <span class="footer-content-font">下载中心</span>
                  </el-link>
                </div>
                <div>
                  <el-link href="https://element.eleme.io" target="_blank">
                    <span class="footer-content-font">服务中心</span>
                  </el-link>
                </div>
                <div>
                  <el-link href="https://element.eleme.io" target="_blank">
                    <span class="footer-content-font">下载中心</span>
                  </el-link>
                </div>
              </div>
              <div>
                <div>
                  <span class="footer-title-font">新闻中心</span>
                </div>

                <div>
                  <el-link href="https://element.eleme.io" target="_blank">
                    <span class="footer-content-font">公司要闻</span>
                  </el-link>
                </div>
                <div>
                  <el-link href="https://element.eleme.io" target="_blank">
                    <span class="footer-content-font">市场前沿</span>
                  </el-link>
                </div>
                <div>
                  <el-link href="https://element.eleme.io" target="_blank">
                    <span class="footer-content-font">技术交流</span>
                  </el-link>
                </div>
                 <div>
                  <el-link href="https://element.eleme.io" target="_blank">
                    <span class="footer-content-font">媒体关注</span>
                  </el-link>
                </div>
              </div>


              <div>
                <div>
                  <span class="footer-title-font">关于科远</span>
                </div>

                <div>
                  <el-link href="https://element.eleme.io" target="_blank">
                    <span class="footer-content-font">公司历史</span>
                  </el-link>
                </div>
                <div>
                  <el-link href="https://element.eleme.io" target="_blank">
                    <span class="footer-content-font">加入科远</span>
                  </el-link>
                </div>
                <div>
                  <el-link href="https://element.eleme.io" target="_blank">
                    <span class="footer-content-font">加入合作</span>
                  </el-link>
                </div>
                
              </div>


            </div>

            <!----页脚 右侧----->
            <div style="width:20%">
              <div>
                <span class="footer-title-font">联系我们</span>
              </div>

              <div>
                <i class="el-icon-phone footer-icon-size"></i>
                <i class="el-icon-goods footer-icon-size"></i>
                <i class="el-icon-edit footer-icon-size"></i>
              </div>
            </div>
          </div>

          <div style="padding-top:12px;margin-bottom:24px;">
            <span class="footer-content-font">©2018 南京科远智慧科技集团股份有限公司 版权所有 苏ICP备07026162号</span>
          </div>
        </div>
      </el-footer>
    </el-container>
  </div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      activeIndex: "1",
      activeIndex2: "1"
    };
  },
  methods: {
    handleSelect(key, keyPath) {

      this.$route.push()
    }
  }
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

.header-height {
  line-height: 80px;
}

.header-font {
  font-size: 480px;
}

.text {
  font-size: 14px;
}

.item {
  margin-bottom: 18px;
}

.clearfix:before,
.clearfix:after {
  display: table;
  content: "";
}
.clearfix:after {
  clear: both;
}

.box-card {
  width: 480px;
}


.nav-font{
font-size: 18px;
font-weight: bold;
}

.footer-icon-size {
  width: 64px;
  height: 64px;
}

.footer-title-font {
  font-size: 20px;
  line-height: 34px;
  color: white;
  font-weight: bold;
}

.footer-content-font {
  font-size: 18px;
  color: gray;

  line-height: 30px;
}
</style>
