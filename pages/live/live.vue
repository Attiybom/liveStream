<template>
  <view class="live-container" :style="{ height: screenHeight + 'px' }">
    <video
      src="https://qiniu-web-assets.dcloud.net.cn/unidoc/zh/2minute-demo.mp4"
      autoplay
      :controls="false"
      object-fit="fill"
      class="video-Container"
      enable-danmu
      danmu-btn
    ></video>

    <!-- 顶部按钮 -->
    <view class="top-container" :style="`top:`+ statusbarHeight + 'px'">
      <!-- 个人信息/观看详细信息 -->
      <view class="bg-danger" style="height: 80rpx;">


      </view>
    </view>

    <!-- 底部按钮 -->
    <view class="bottom-container"> </view>
  </view>
</template>

<script>
export default {
  data() {
    return {
      screenHeight: 0,// 单位都是px
      statusbarHeight: 0, // 单位都是px
    };
  },
  mounted() {
    this.screenHeight = uni.getSystemInfoSync().windowHeight;
    this.statusbarHeight = uni.getSystemInfoSync().statusBarHeight;
    console.log("statusHeight", this.statusbarHeight);
  },
  methods: {},
};
</script>

<style scoped>
.live-container {
  display: flex;
  background-color: #ffd63a;
}
.video-Container {
  flex: 1;
}

.top-container {
  position: fixed;
  left: 0;
  right: 0;
  background-color: red;
  /* 顶部容器本身的高度 */
  /* height: 80rpx; */
}

.bottom-container {
  position: fixed;
  bottom: 0;
  left: 0;
  right: 0;
  background-color: red;
  height: 120rpx;
}
</style>
