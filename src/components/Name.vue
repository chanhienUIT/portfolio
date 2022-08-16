<template>
  <div class="mt-0 py-8 px-8 max-w-xl mx-auto bg-slate-800 rounded-xl shadow-xl space-y-2 sm:py-4 sm:flex sm:items-center sm:space-y-0 sm:space-x-6">
    <img class="block mx-auto h-24 rounded-full sm:mx-0 sm:shrink-0" src="../assets/image.jpg">
    <div class="text-center space-y-2 sm:text-left">
      <div class="space-y-0.5">
        <div class="flex items-center justify-center mt-4 space-x-4">
          <transition name="fade" mode="out-in">
            <div @click="nameToggle = !nameToggle" v-if="nameToggle" class="text-4xl align-middle cursor-pointer">
              <a class="font-bold text-slate-300 mr-2">Hồng Chấn</a>
              <a class="font-extrabold text-slate-200">Hiển</a>
            </div>
            <div @click="nameToggle = !nameToggle" v-else class="text-4xl align-middle cursor-pointer">
              <a class="font-bold text-slate-300 mr-2">ホン チャン ヒエン</a>
            </div>
          </transition>
          <a>
            <img class="h-5 inline-flex align-middle" src="../assets/vn.svg">
          </a>
        </div>
        <div>
          <p class="text-lg text-slate-400 py-1">
            Junior Web Developer in 東京都
          </p>
          <div class="block mx-auto align-center justify-left space-x-4 sm:mx-0 sm:shrink-0">
            <img class="h-6 inline-flex" src="../assets/vue.png">
            <img class="h-6 inline-flex" src="../assets/laravel.svg">
            <div class="h-7 inline-flex align-middle">
              <img @click="showMail = !showMail" class="rounded-md cursor-pointer transition ease-in-out delay-150 hover:-translate-y-1 hover:scale-110 duration-300" src="../assets/mail.svg">
              <transition name="slide-fade">
                <input v-if="showMail" type="text" class="ml-3 bg-gray-100 border border-gray-300 text-gray-900 text-sm rounded-lg focus:ring-blue-500 focus:border-blue-500 block w-full p-2.5 cursor-not-allowed bg-gray-700 border-gray-600 placeholder-gray-400 text-gray-400 focus:ring-blue-500 focus:border-blue-500" value="chanhien050@gmail.com" disabled>
              </transition>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
  export default {
  data() {
    return {
      nameToggle: true,
      showMail: false
    };
  },

};
</script>

<style scoped>
  .slide-fade-enter-active, .slide-fade-enter, .slide-fade-leave-active, .fade-enter-active, .fade-leave-active {
    transition: all .15s ease;
  }
  .slide-fade-leave-to, .slide-fade-enter-from
  /* .slide-fade-leave-active below version 2.1.8 */ {
    transform: translateX(-10px);
    opacity: 0;
  }
  .fade-enter, .fade-leave-to
  /* .component-fade-leave-active below version 2.1.8 */ {
    opacity: 0;
  }
</style>