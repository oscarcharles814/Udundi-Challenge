<script setup>
const props = defineProps(['onClose'])
</script>

<template>
  <div class="overflow-y-auto overflow-x-hidden fixed top-0 right-0 left-0 z-50 justify-center items-center w-full md:inset-0 h-[calc(100%-1rem)] max-h-full">
    <div class="relative p-4 w-full sm:max-w-xl max-w-screen-sm max-h-full top-[50%] translate-y-[-50%] lg:left-[140px] sm:left-[70px]">
      <!-- Modal content -->
      <div class="relative bg-white p-8">
        <!-- Modal header -->
        <div class="flex items-center justify-between p-4 md:p-5">
          <h3 class="text-[66px] font-[Didot] text-[#611818] font-semibold dark:text-white">
              Explore
          </h3>
          <button type="button" class="absolute right-5 top-5 text-gray-400 bg-transparent hover:bg-gray-200 hover:text-gray-900 rounded-lg text-sm w-8 h-8 ms-auto inline-flex justify-center items-center dark:hover:bg-gray-600 dark:hover:text-white" @click="onClose">
            <svg class="w-3 h-3" aria-hidden="true" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 14 14">
              <path stroke="#611818" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="m1 1 6 6m0 0 6 6M7 7l6-6M7 7l-6 6"/>
            </svg>
            <span class="sr-only">Close modal</span>
          </button>
        </div>
        <!-- Modal body -->
        <div class="p-4 md:p-5 space-y-4">
          <p class="text-base leading-relaxed text-[#282828] font-[Lato]">
            Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium, totam rem aperiam, eaque ipsa quae ab illo inventore veritatis et quasi architecto beatae vitae dicta sunt explicabo. Nemo enim ipsam voluptatem quia voluptas sit aspernatur aut odit aut fugit, sed quia consequuntur magni dolores eos qui ratione voluptatem sequi nesciunt. Neque porro quisquam est, qui dolorem ipsum quia dolor sit amet, consectetur, adipisci velit, sed quia non numquam eius modi tempora incidunt ut labore et dolore magnam aliquam quaerat voluptatem. Ut enim ad minima veniam, quis nostrum exercitationem ullam corporis suscipit laboriosam, nisi ut aliquid ex ea commodi consequatur? 
          </p>
        </div>
        <!-- Modal footer -->
        <div class="flex items-center p-4 md:p-5">
          <button type="button" class="font-[Lato] rounded-none px-12 py-2 text-[18px] font-semibold text-white uppercase bg-gradient-to-r from-[#611818] to-[#A36754]">Read More</button>
        </div>
      </div>
    </div>
  </div>
</template>
