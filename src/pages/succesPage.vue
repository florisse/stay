<template>
  <div
    class="bg-white px-6 pt-40 md:p-10 md:rounded-3xl md:h-fit h-screen w-full md:w-[344px]"
  >
    <img src="../assets/checkBig.svg" alt="" class="pb-4 md:w-fit w-[60px]" />
    <span class="text-4xl text-[#242742] font-bold"
      >Thanks for subscribing !</span
    >
    <div class="py-3">
      <span class="md:text-[10px] text-[14px] leading-3"
        >A confirmation email has been sent to
        <span class="font-bold text-[#242742]">ash@loremcompany.com.</span>
        Please open it and click the button inside to confirm your subscription.
      </span>
    </div>

    <button
      class="md:mt-4 mt-[200px] text-sm bg-[#242742] text-white font-bold p-3 rounded-md hover:shadow hover:bg-gradient-to-r from-pink-500 to-[#ff4a3d] w-full"
    >
      Dismiss message
    </button>
  </div>
</template>
<script setup></script>
<style scoped>
button:hover {
  filter: drop-shadow(0px 10px 8px rgba(255, 74, 61, 0.52));
}
</style>
