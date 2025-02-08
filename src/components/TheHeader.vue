<script setup lang="ts">
import { RouterLink } from 'vue-router'
import NeonSharkoLogo from '@/assets/img/icon.png'

type Link = {
  target: string
  text: string
}

const links: Link[] = [
  { target: '/', text: 'Home' },
  { target: '/about', text: 'About' },
  { target: '/links', text: 'Links' },
]
</script>

<template>
  <header
    class="fixed w-full top-0 left-0 flex justify-between items-center p-6 text-lg bg-white dark:bg-black shadow-md shadow-neutral-500/10"
  >
    <RouterLink to="/" class="flex gap-4 align-center">
      <img class="w-8 h-8 rounded-full" :src="NeonSharkoLogo" alt="NeonSharko Logo" />
      <h1>NeonSharko</h1>
    </RouterLink>

    <nav>
      <ul class="flex flex-row gap-4">
        <li v-for="(link, i) in links" :key="i">
          <RouterLink :to="link.target">
            {{ link.text }}
          </RouterLink>
        </li>
      </ul>
    </nav>
  </header>
</template>

<style scoped lang="scss"></style>
