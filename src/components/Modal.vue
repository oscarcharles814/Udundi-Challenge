<script setup>
const props = defineProps(['onClose'])
</script>

<template>
  <div class="overflow-y-auto overflow-x-hidden fixed top-0 right-0 left-0 z-50 justify-center items-center w-full md:inset-0 h-[calc(100%-1rem)] max-h-full">
    <div class="relative max-w-[580px]  top-[50%] translate-y-[-50%] xl:left-[140px] lg:left-[110px] sm:left-[45px] left-[50%] sm:translate-x-[0] translate-x-[-50%] sm:p-0 p-[15px]">
      <!-- Modal content -->
      <div class="relative bg-white sm:pt-[72px] sm:pr-[72px] sm:pb-[78px] sm:pl-[66px] p-[48px] shadow-[0_17px_25.3px_7px_rgba(0,0,0,0.10)]">
        <!-- Modal header -->
        <div class="flex items-center justify-between">
          <h3 class="text-[66px] font-[Didot] text-[#611818] font-semibold leading-[85px] dark:text-white">
              Explore
          </h3>
          <div class="absolute right-[25px] top-[25px] w-[15px] h-[15px] cursor-pointer" @click="onClose">
            <svg class="w-[15px] h-[15px] min-w-[15px]" aria-hidden="true" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 14 14">
              <path stroke="#611818" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="m1 1 6 6m0 0 6 6M7 7l6-6M7 7l-6 6"/>
            </svg>
            <span class="sr-only">Close modal</span>
          </div>
        </div>
        <!-- Modal body -->
        <div class="pt-[26px] space-y-4 sm:max-h-[70vw] max-h-[88vw] overflow-auto">
          <p class="leading-[22px] text-[#282828] text-[18px] font-[Lato] mb-[15px] tracking-[0.35px]">
            Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium, totam rem aperiam, eaque ipsa quae ab illo inventore veritatis et quasi architecto beatae vitae dicta sunt explicabo. Nemo enim ipsam voluptatem quia voluptas sit aspernatur aut odit aut fugit, sed quia consequuntur magni dolores eos qui ratione voluptatem sequi nesciunt. Neque porro quisquam est, qui dolorem ipsum quia dolor sit amet, consectetur, adipisci velit, sed quia non numquam eius modi tempora incidunt ut labore et dolore magnam aliquam quaerat voluptatem. Ut enim ad minima veniam, quis nostrum exercitationem ullam corporis suscipit laboriosam, nisi ut aliquid ex ea commodi consequatur?  
          </p>
        </div>
        <!-- Modal footer -->
        <div class="flex items-center pt-[29px]">
          <button type="button" class="border-none font-[Lato] rounded-none pt-[16px] pr-[58px] pb-[15px] pl-[57px] text-[18px] font-semibold leading-[22px] text-white uppercase bg-gradient-to-r from-[#611818] to-[#A36754] tracking-[1.7px]">Read More</button>
        </div>
      </div>
    </div>
  </div>
</template>
