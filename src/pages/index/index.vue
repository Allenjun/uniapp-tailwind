<template>
   <view class="content h-screen bg-gray-200 " :class="{'dark':darkMode}">
      <image class="logo w-16 h-16" src="/static/logo.png"></image>
      <view>
         <view class="title p-2 rounded text-lg flex flex-col">
            <div class="bg-gray-200 p-2 rounded shadow-lg m-2"> {{title}}</div>
            <div class="bg-yellow-300  text-white p-2 rounded shadow-lg m-2">
               {{title}}
            </div>
         </view>
         <button class=" btn shadow-lg">
            登录</button>
      </view>
      <div class="mt-2 dark--bg-black flex flex-row justify-between w-screen flex-wrap">
         <div class="m-2 card zoom-in shadow-lg bg-red-400 text-blue-500 w-1_3 dark--text-red-500">
            1</div>
         <div class="m-2 bg-red-400 text-white w-1_3">
            1</div>
         <div class="m-2  text-white w-1_3">
            <button class=" bg-red-500 text-white" disabled>
               Submit
            </button>
            1
         </div>
         <button class="m-2 zoom-in w-32 h-32 bg-white dark--bg-indigo-700 dark--text-white  flex justify-center items-center rounded-full" @tap="toggleDark">
            D
         </button>

      </div>
      <div>
         <view class="uni-padding-wrap uni-common-mt">
            <button type="primary">页面主操作 Normal</button>
            <button type="primary" loading="true">页面主操作 Loading</button>
            <button type="primary" disabled="true">页面主操作 Disabled</button>
            <button type="default">页面次要操作 Normal</button>
            <button type="default" disabled="true">页面次要操作 Disabled</button>
            <button type="warn">警告类操作 Normal</button>
            <button type="warn" disabled="true">警告类操作 Disabled</button>
            <view class="button-sp-area">
               <button type="primary" plain="true">按钮</button>
               <button type="primary" disabled="true" plain="true">不可点击的按钮</button>
               <button type="default" plain="true">按钮</button>
               <button type="default" disabled="true" plain="true">按钮</button>
               <button class="mini-btn" type="primary" size="mini">按钮</button>
               <button class="mini-btn" type="default" size="mini">按钮</button>
               <button class="mini-btn" type="warn" size="mini">按钮</button>
            </view>
         </view>
      </div>
   </view>
</template>

<script>
export default {
   data() {
      return {
         title: "Hello",
         darkMode: false,
      };
   },
   onLoad() {},
   methods: {
      toggleDark() {
         this.darkMode = !this.darkMode;
      },
   },
};
</script>

<style lang="scss">
.content {
   @apply flex flex-col items-center justify-center;
}

.btn {
   @apply px-4 py-2 rounded  text-white bg-green-500 text-xl;
   &:active {
      @apply bg-green-600 border-blue-500;
   }
}

.card {
   @apply px-5 py-6 rounded-md bg-white overflow-hidden;
}

.zoom-in {
   @apply transform transition ease-in-out duration-300;
}

.zoom-in:active {
   @apply scale-110;
}
</style>
