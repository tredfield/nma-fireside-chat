<script setup lang="ts">
withDefaults(defineProps<{
  mode?: string
  photo?: string
  photoAlt?: string
  photoPosition?: string
}>(), { mode: 'paper', photoPosition: 'center' })

const asset = (path?: string) => path ? import.meta.env.BASE_URL + path.replace(/^\//, '') : ''
</script>

<template>
  <section class="slidev-layout nma-slide" :class="`mode-${mode}`">
    <img v-if="photo" class="scene" :src="asset(photo)" :alt="photoAlt || ''" :style="{ objectPosition: photoPosition }" />
    <div v-if="photo" class="photo-shade" aria-hidden="true" />
    <div class="slide-content"><slot /></div>
    <img class="brand-mark" src="/brand/nma-logo.png" alt="Northwest Motorcycle Association" />
  </section>
</template>
