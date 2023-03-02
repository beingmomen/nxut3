<template>
  <div class="flex items-center flex-col p-10 bg-gray-100 h-screen">
    <h2 class="font-black text-3xl mb-6">Nuxt</h2>
    <div class="flex w-full justify-center flex-row flex-grow gap-6">
      <div
        class="basis-1/4 h-screen bg-white p-4 flex justify-center rounded-md"
      >
        <h3 class="">Chapter</h3>
      </div>
      <div class="basis-3/4 h-screen bg-red-100 p-4 rounded-md">
        <NuxtPage />
      </div>
    </div>
  </div>
</template>

<script setup>
</script>

<style lang="scss" scoped>
</style>