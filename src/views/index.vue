<template>
  <div id="layout">
    <div class="block">
      <el-carousel height="500px">
        <el-carousel-item v-for="item in banners" :key="item">
          <img :src="item.url" />
        </el-carousel-item>
      </el-carousel>
    </div>

    <div style="fontSize:36px;textAlign: left;margin-left:24px">新闻中心</div>

    <el-carousel :interval="4000" type="card" height="200px">
      <el-carousel-item v-for="item in banners" :key="item">
        <img :src="item.url" />
      </el-carousel-item>
    </el-carousel>

    <div>
      <div style="fontSize:36px;textAlign: left;margin-left:24px">产品中心</div>

      <el-row>
        <el-col :span="8" v-for="(o, index) in 2" :key="o" :offset="index > 0 ? 2 : 0">
          <el-card :body-style="{ padding: '0px' }">
            <img
              src="https://shadow.elemecdn.com/app/element/hamburger.9cf7b091-55e9-11e9-a976-7f4d0b07eef6.png"
              class="image"
            />
            <div style="padding: 14px;">
              <span>好吃的汉堡</span>
              <div class="bottom clearfix">
                <time class="time">{{ currentDate }}</time>
                <el-button type="text" class="button">操作按钮</el-button>
              </div>
            </div>
          </el-card>
        </el-col>
      </el-row>
    </div>
  </div>
</template>

<script>
export default {
  name: "Index",
  banners: "",
  data() {
    return {
      banners: [
        {
          url: require("../assets/banner-1.jpg")
        },
        {
          url: require("../assets/banner-2.jpg")
        },
        {
          url: require("../assets/banner-3.jpg")
        },
        {
          url: require("../assets/banner-3.jpg")
        },
        {
          url: require("../assets/banner-3.jpg")
        },
        {
          url: require("../assets/banner-3.jpg")
        }
      ]
    };
  }
};
</script>


<style scoped>
#layout {
  width: 100%;
}

.el-carousel__item h3 {
  color: #475669;
  font-size: 14px;
  opacity: 0.75;
  line-height: 150px;
  margin: 0;
}

.el-carousel__item:nth-child(2n) {
  background-color: #99a9bf;
}

.el-carousel__item:nth-child(2n + 1) {
  background-color: #d3dce6;
}

.time {
  font-size: 13px;
  color: #999;
}

.bottom {
  margin-top: 13px;
  line-height: 12px;
}

.button {
  padding: 0;
  float: right;
}

.image {
  width: 100%;
  display: block;
}

.clearfix:before,
.clearfix:after {
  display: table;
  content: "";
}

.clearfix:after {
  clear: both;
}
</style>