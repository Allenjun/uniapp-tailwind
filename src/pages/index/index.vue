<template>
   <view class="content">
      <image class="logo w-32 h-32" src="/static/logo.png"></image>
      <view>
         <view class="title p-4 rounded text-lg flex flex-col">
            <div class="bg-gray-200 p-4 rounded shadow-lg m-4"> {{title}}</div>
            <div class="bg-yellow-300  text-white p-4 rounded shadow-lg m-4">
               {{title}}
            </div>
         </view>
         <button class="px-4 py-2 rounded  border-0 text-white bg-green-500 text-xl shadow-lg">
            登录</button>
      </view>
      <div class="flex space-x-4">
         <div class="bg-red-400 text-white hover:bg-red-600">
            1</div>
         <div class="bg-green-600">2</div>
         <div class="bg-green-600">3</div>
         <div>4</div>
         <div>5</div>
      </div>
   </view>
</template>

<script>
export default {
   data() {
      return {
         title: "Hello",
      };
   },
   onLoad() {},
   methods: {},
};
</script>

<style lang="scss">
.content {
   @apply flex flex-col items-center justify-center;
}
</style>
