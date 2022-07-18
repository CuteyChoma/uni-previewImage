<!--
 * @Author: choma
 * @Date: 2022-07-18 15:46:09
 * @LastEditTime: 2022-07-18 17:14:14
 * @LastEditors: choma
 * @Description:  
 * @FilePath: \014-uni-vite\src\pages\index\index.vue
-->
<template>
  <view class="content">
    <image class="logo" :src="current" @tap="previewImage(current)" />
  </view>
</template>

<script setup lang="ts">
const current =
  "https://vip.hangshida-pd.com:8021/images/2022/07/14/562ac469-ac7b-4105-acc4-9c49e789712b.png";
const previewImage = (current: string) => {
  const urls = [
    "https://vip.hangshida-pd.com:8021/images/2022/07/14/562ac469-ac7b-4105-acc4-9c49e789712b.png",
    "https://vip.hangshida-pd.com:8021/images/2022/07/14/c329c7c4-5ed4-436d-8381-3f146b2467cc.png",
    "https://vip.hangshida-pd.com:8021/images/2022/07/14/4216a664-4995-4583-b311-bd70cdf01e70.png",
  ];
  uni.previewImage({
    current,
    urls,
    success: (result) => {
      console.log("result: ", result);
    },
    fail: (error) => {
      console.log("error: ", error);
    },
  });
};
</script>

<style>
.content {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}

.logo {
  height: 200rpx;
  width: 200rpx;
  margin-top: 200rpx;
  margin-left: auto;
  margin-right: auto;
  margin-bottom: 50rpx;
}

</style>
