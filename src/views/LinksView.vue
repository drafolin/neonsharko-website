<script setup lang="ts">
import Divider from '@/assets/img/spacer.svg'
import Kofi from '@/assets/img/kofi_symbol.svg?url'
import Twitch from '@/assets/img/glitch_flat_purple.svg?url'
import Youtube from '@/assets/img/yt_icon_rgb.ai.svg?url'
import TikTok from '@/assets/img/TikTok-Social-Icon-Color-White.svg?url'
import Instagram from '@/assets/img/Instagram_Glyph_Gradient.svg?url'

type Link = {
  target: string
  text: string
  image: string
}

const links: Link[] = [
  {
    target: 'https://www.tiktok.com/@neonsharko',
    text: 'TikTok',
    image: TikTok,
  },
  {
    target: 'https://ko-fi.com/neonsharko',
    text: 'Ko-fi',
    image: Kofi,
  },
  {
    target: 'https://www.twitch.tv/neonsharko',
    text: 'Twitch',
    image: Twitch,
  },
  {
    target: 'https://twitter.com/N3OStarblazer',
    text: 'Twitter',
    image: 'https://cdn.worldvectorlogo.com/logos/twitter-3.svg',
  },
  {
    target: 'https://www.youtube.com/@N3OSTARBLAZER',
    text: 'YouTube',
    image: Youtube,
  },
  {
    target: 'https://www.instagram.com/neonsharko',
    text: 'Instagram',
    image: Instagram,
  },
]
</script>

<template>
  <main class="flex flex-col items-center">
    <section class="hero py-[15vh] flex flex-col items-center">
      <h1 class="text-5xl font-semibold my-12">Links</h1>

      <section class="w-fit">
        <p>Here is a collection of link to other media platforms you can find me on !</p>
      </section>
    </section>

    <section class="w-full flex flex-col items-center">
      <ul
        class="grid grid-cols-2 md:grid-cols-3 gap-12 max-w-4xl w-full justify-items-center items-stretch"
      >
        <li v-for="(link, i) in links" :key="i" class="card w-40">
          <a
            :href="link.target"
            class="flex flex-col items-center justify-between py-10 px-10 w-full h-full"
          >
            <img :src="link.image" :alt="link.text" class="grow" />
            <span class="mt-4">{{ link.text }}</span>
          </a>
        </li>
      </ul>
    </section>

    <Divider class="w-20 my-20" />
  </main>
</template>
