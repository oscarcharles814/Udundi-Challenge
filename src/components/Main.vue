<script setup>
  import {onMounted, ref} from 'vue'
  import Modal from './Modal.vue'

  const isBannerLoaded = ref(false);

  function handleBannerLoad () {
    isBannerLoaded.value = true;
  }

  onMounted(() => {
    const bannerImage = document.getElementById('bannerImage');
    bannerImage.addEventListener('load', handleBannerLoad);
  })

  const isOpen = ref(false);
  function openModal(_event) {
    isOpen.value = true;
  }
  function onClose(_event) {
    isOpen.value = false;
  }
</script>

<template>
  <img id="bannerImage" class="hidden" src="../assets/background.webp">
  <div v-if="isBannerLoaded" id="bannerImage" class="relative w-screen h-screen bg-[url('./assets/background.webp')] bg-cover bg-no-repeat">
    <div class="w-[28.7%] h-screen bg-[#611818]" />
    <div
      id="title"
      class="absolute bottom-[222px] left-[13%]"
    >
      <p class="animated-text font-[Didot] text-white  xl:text-[224px] text-[15.5vw] leading-none" v-if="!isOpen">Explore</p>
      <div class="flex cursor-pointer items-center" @click="openModal">
        <img src="../assets/Plus.svg" alt="plus" class="md:w-[43px] md:h-[43px] w-[32px] h-[32px]"/>
        <p
          class="sm:ml-[23px] ml-4 font-[Lato] text-white sm:text-[25px] text-[20px]"
        >
          More Details
        </p>
      </div>
    </div>
    <div
      id="social-buttons"
      class="absolute right-[31px] bottom-[39px]"
    >
      <a href="#"><img class="md:mb-[20px] mb-[12px] md:w-[68px] md:h-[67px] w-[48px] h-[48px] drop-shadow-[2px_2px_3px_rgba(0,0,0,0.5)]" src="../assets/Facebook.svg" alt="facebook" /></a>
      <a href="#"><img class="md:w-[67px] md:h-[68px] w-[48px] h-[48px] drop-shadow-[2px_2px_3px_rgba(0,0,0,0.5)]" src="../assets/Instagram.svg" alt="instagram" /></a>
    </div>
  </div>
  
  <transition name="fade">
    <Modal
      v-if="isOpen"
      :onClose="onClose"
    />
  </transition>
  
</template>

<style scoped>
.fade-enter-active,
.fade-leave-active {
  transition: transform 1s ease;
}

.fade-enter-to,
.fade-leave-from {
  transform: scale(1);
  transform-origin: 13% calc(100% - 210px);
}

.fade-enter-from,
.fade-leave-to {
  transform: scale(0);
  transform-origin: 13% calc(100% - 210px);
}

.animated-text {
  animation: fadeInUp 1s ease;
}

@keyframes fadeInUp {
  from {
    opacity: 0;
    transform: translateY(200px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

</style>
