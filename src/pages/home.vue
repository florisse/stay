<template>
  <div
    v-if="!success"
    class="bg-white w-screen md:w-fit md:rounded-3xl md:p-4 md:flex-row flex-col-reverse flex items-center"
  >
    <div class="md:p-10">
      <div class="px-6 py-6 md:p-0">
        <span
          class="text-[#242742] text-[40px] font-semibold md:font-bold md:text-[50px]"
        >
          Stay updated !
        </span>
      </div>
      <Check />
      <Email @submit="submitForm" />
    </div>
<div :class="animate" class="w-[400px] flex-shrink-0 h-[593px] bg-slate-700   rounded-2xl">
  <img class="md:flex hidden" src="../assets/illustation.svg" alt="" @load="animate=''"  loading="lazy"/>

</div>    <div class="flex items-center w-full">
      <img class="md:hidden w-full flex" src="../assets/mobil.svg" alt="" loading="lazy" />
    </div>
  </div>
  <div v-else>
    <Success />
  </div>
</template>

<script setup>
import Success from "../pages/succesPage.vue";
import Check from "../components/checkPart.vue";
import Email from "../components/emailPart.vue";
import { ref } from "vue";
const success = ref(false);
const animate = ref('animate-pulse')
function submitForm() {
  console.log("form submitted");
  success.value = true;
}
</script>

<style></style>
