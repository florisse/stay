<template>
  <div class="grid gap-4 px-6 md:p-0 pb-6">
    <div class="flex justify-between items-center">
      <span class="text-sm font-semibold">Email adress</span>
      <span class="text-[#ff6257] text-sm font-semibold" v-if="error"
        >Valid email required</span
      >
    </div>
    <form class="w-full grid gap-4" @submit.prevent="submit">
      <input
        :class="
          error
            ? 'border-[#ff6257] bg-[#ff4a3d] bg-opacity-10'
            : 'border-[#9294a0]'
        "
        v-model="email"
        placeholder="email@company.com"
        type="email"
        class="w-full p-3 rounded border outline-none"
      />

      <!-- :class="index === 5 || index === 6 ? 'red-color' : ''" -->
      <button
        type="submit"
        class="bg-[#242742] text-white font-semibold w-full rounded p-3"
      >
        Subscribe to monthly newsletter
      </button>
    </form>
  </div>
</template>

<script setup>
import { ref } from "vue";

const email = ref("");
const error = ref(false);
const emit = defineEmits(["submit"]);

function submit() {
  if (!email.value.length || !ValidateEmail(email.value)) {
    error.value = true;
  } else {
    error.value = false;
    emit("submit");
  }
  console.log(email.value);
}
function ValidateEmail(mail) {
  if (/^\w+([\.-]?\w+)*@\w+([\.-]?\w+)*(\.\w{2,3})+$/.test(mail)) {
    return true;
  }
  return false;
}
</script>

<style></style>
