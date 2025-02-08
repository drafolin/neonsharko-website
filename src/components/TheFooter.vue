<script setup lang="ts">
const currentYear = new Date().getFullYear()
</script>

<template>
  <footer class="bg-gray-500/20 p-10 text-center">
    <section>
      <p>
        <span>&copy; 2025{{ currentYear !== 2025 ? `- ${currentYear}` : '' }} NeonSharko.</span>
        <span> All rights reserved. </span>
      </p>
      <p>
        Made with <a href="https://vuejs.org" class="text-green-600">VueJS</a> and
        <span class="text-red-500/70">&hearts;</span> by
        <a href="https://derg.ch" class="text-[#7655e3]">Dråfølin</a>
      </p>
    </section>
  </footer>
</template>

<style scoped></style>
