<template>
   <view class="content" :class="{'dark':darkMode}">
      <image class="logo w-32 h-32" src="/static/logo.png"></image>
      <view>
         <view class="title p-4 rounded text-lg flex flex-col">
            <div class="bg-gray-200 p-4 rounded shadow-lg m-4"> {{title}}</div>
            <div class="bg-yellow-300  text-white p-4 rounded shadow-lg m-4">
               {{title}}
            </div>
         </view>
         <button class=" btn shadow-lg">
            登录</button>
      </view>
      <div class="flex flex-row justify-between w-full flex-wrap space-x-4">
         <div class="btn bg-red-400 text-white w-1_3 dark--text-red-500">
            1</div>
         <div class="bg-red-400 text-white w-1_3">
            1</div>
         <div class="bg-red-400 text-white w-1_3">
            1</div>
         <div class=" m-4 w-32 bg-white dark--bg-indigo-700 dark--text-white h-32 flex justify-center items-center rounded-full" @tap="toggleDark">
            D
         </div>
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
</style>
