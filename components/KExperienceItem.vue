<script setup lang="ts">
const props = defineProps<{
  title: string
  date: string
  skills: string[],
  texts: string[],
  link: string | null
}>()

const hover = ref(false)
</script>

<template>
  <ULink as="div" :to="link" target="_blank" class="flex" :class="{ 'bg-cyan-100 bg-opacity-10': hover }"
         @mouseover="hover = true" @mouseout="hover = false">
    <div class="basis-1/4">{{ date }}</div>
    <div class="basis-3/4">
      <h3 class="text-xl font-bold flex items-center" :class="{ 'text-cyan-500': hover && link }">
        <span class="mr-2">{{ title }}</span>
        <UIcon v-if="link" name="i-material-symbols-arrow-outward"
               class="transition-transform" :class="{ '-translate-y-1 translate-x-1': hover }"/>
      </h3>
      <p v-for="p in texts" class="mt-4">{{ p }}</p>
      <div class="mt-4 flex flex-wrap gap-2">
        <UBadge v-for="skill in skills" color="cyan" variant="subtle" :ui="{ rounded: 'rounded-full' }">{{ skill }}</UBadge>
      </div>
    </div>
  </ULink>
</template>