<template>
  <div id="app">
    <el-container>
      <el-header
        height="100px"
        style="display:flex;justify-content:space-between;padding: 0 16vw;align-items: center"
      >
        <div style="display:flex;width:18vw;justify-content:space-around">
          <div>Hi，欢迎来到OurFarm</div>
          <div>登陆</div>
          <div>立即注册</div>
        </div>
        <div style="display:flex;width:30vw;justify-content:space-around">
          <div>首页</div>
          <div>关于我们</div>
          <div>客房</div>
          <div>餐饮</div>
          <div>附加服务</div>
        </div>
      </el-header>
      <el-main>
        <el-carousel :interval="50000" arrow="always" height=45vh>
          <el-carousel-item v-for="item in carouselList" :key="item">
            <!-- <img :src="'./assets/{{item}}.jpg'" /> -->
            <img :src="require('./assets/'+item+'.jpg')" style="height:45vh"/>
          </el-carousel-item>
        </el-carousel>
      </el-main>
    </el-container>
  </div>
</template>
<script>
// import HelloWorld from "./components/HelloWorld.vue";
export default {
  name: "app",
   data () {
    return {
      carouselList: ["Carousel1", "Carousel2", "Carousel3"]
    }
  },
  components: {
    // HelloWorld
  }
};
</script>
<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  /* margin-top: 60px; */
}
.el-header,
.el-footer {
  background-color: #b3c0d1;
  color: #333;
  text-align: center;
  line-height: 60px;
}

.el-aside {
  background-color: #d3dce6;
  color: #333;
  text-align: center;
  line-height: 200px;
}

.el-main {
  background-color: #e9eef3;
  color: #333;
  text-align: center;
  line-height: 160px;
  padding-top: 3px;
}

.el-carousel__item h3 {
  color: #475669;
  font-size: 18px;
  opacity: 0.75;
  line-height: 300px;
  margin: 0;
}

.el-carousel__item:nth-child(2n) {
  background-color: #99a9bf;
}

.el-carousel__item:nth-child(2n + 1) {
  background-color: #d3dce6;
}

body > .el-container {
  margin-bottom: 40px;
}

.el-container:nth-child(5) .el-aside,
.el-container:nth-child(6) .el-aside {
  line-height: 260px;
}

.el-container:nth-child(7) .el-aside {
  line-height: 320px;
}
</style>
