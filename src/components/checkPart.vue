<template>
  <div class="w-[400px] px-6 md:p-0">
    <span class="text-center text-base"
      >Join 60,000+ product managers receiving monthly updates on:</span
    >
    <div class="py-4">
      <div
        class="check flex py-2 space-x-4"
        v-for="(item, index) in dataTable"
        :key="index"
      >
        <img src="../assets/check.svg" alt="" />
        <span>
          {{ item.title }}
        </span>
      </div>
    </div>
  </div>
</template>

<script setup>
const dataTable = [
  {
    title: "Product discovery and building what matters",
  },
  {
    title: "Measuring to ensure updates are a success",
  },
  {
    title: "And much more!",
  },
];
</script>

<style></style>
