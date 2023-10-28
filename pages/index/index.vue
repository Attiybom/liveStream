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

    <!-- 图片列表-瀑布流 -->
    <view class="flex flex-wrap">
      <template v-for="item in 10" :key="item">
        <view class="img-container rounded" >
          <!-- 背景图片本身 -->
          <image
            class="img-size"
            src="../../static/demo/1.jpg"
            mode="aspectFill"
          ></image>
          <!-- 左上积分 -->
          <view class="rounded-circle left-top-icon px-2 flex align-center">
            <text class="iconfont icon-jifen- text-warning mr-1"></text>
            <text class="text-white font-sm">0</text>
          </view>
          <!-- 右上角人气 -->
          <view class="rounded-circle right-top-icon px-2 flex align-center">
            <text class="font-sm text-white">人气：</text>
            <text class="text-white font-sm">0</text>
          </view>
          <!-- 左下标题 -->
          <view class="rounded-circle left-bottom-icon px-2 flex align-center">
            <text class="font-sm text-white">标题</text>
          </view>
          <view class="rounded-circle right-bottom-icon px-2 flex align-center">
            <text class="circle-icon rounded-circle bg-danger mr-1"></text>
            <text class="text-white font-sm">已结束</text>
          </view>
        </view>
      </template>
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

.left-top-icon {
  position: absolute;
  left: 15rpx;
  top: 15rpx;
  background-color: rgba(0, 0, 0, 0.4);
}
.right-top-icon {
  position: absolute;
  right: 15rpx;
  top: 15rpx;
  background-color: rgba(0, 0, 0, 0.4);
}
.left-bottom-icon {
  position: absolute;
  left: 15rpx;
  bottom: 15rpx;
}
.right-bottom-icon {
  position: absolute;
  right: 15rpx;
  bottom: 15rpx;
  background-color: rgba(0, 0, 0, 0.4);
}
.circle-icon {
  width: 20rpx;
  height: 20rpx;
}
</style>
