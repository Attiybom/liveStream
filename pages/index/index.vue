<template>
  <view class="">
    <!-- 顶部轮播图部分 -->
    <swiper
      :indicator-dots="true"
      :autoplay="true"
      :interval="3000"
      :duration="500"
      class="banner-size"
    >
      <swiper-item>
        <view class="swiper-item">
          <image
            class="banner-size"
            src="../../static/demo/banner/1.jpg"
            mode=""
          ></image>
        </view>
      </swiper-item>
      <swiper-item>
        <view class="swiper-item">
          <image
            class="banner-size"
            src="../../static/demo/banner/2.jpg"
            mode=""
          ></image>
        </view>
      </swiper-item>
    </swiper>

    <!-- 瀑布流 -->
    <view class="flex flex-wrap">
      <view class="img-container rounded">
        <image
          class="img-size"
          src="../../static/demo/1.jpg"
          mode="aspectFill"
        ></image>
        <view class="rounded-circle left-icon px-2 flex align-center">
          <text class="iconfont icon-jifen- text-warning mr-1" ></text>
		  <text class="text-white font">0</text>
        </view>
      </view>
      <view class="img-container">
        <image
          class="img-size"
          src="../../static/demo/1.jpg"
          mode="aspectFill"
        ></image>
      </view>
      <view class="img-container">
        <image
          class="img-size"
          src="../../static/demo/1.jpg"
          mode="aspectFill"
        ></image>
      </view>
      <view class="img-container">
        <image
          class="img-size"
          src="../../static/demo/1.jpg"
          mode="aspectFill"
        ></image>
      </view>
    </view>
  </view>
</template>

<script>
export default {
  data() {
    return {
      title: "Hisasd, liveStream!!!",
    };
  },
  onLoad() {},
  methods: {},
};
</script>

<style scoped>
.banner-size {
  width: 750rpx;
  height: 250rpx;
}

.img-container {
  box-sizing: border-box;
  position: relative;
  width: 375rpx;
  padding: 5rpx;
}

.img-size {
  width: 365rpx;
  height: 365rpx;
}

.left-icon {
  position: absolute;
  left: 15rpx;
  top: 15rpx;
  background-color: rgba(0, 0, 0, 0.4);
}
</style>
