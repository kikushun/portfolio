<script setup lang="ts">
const links = [{
  label: '自己紹介',
  icon: 'i-mdi-face-man-profile',
  color: 'text-cyan-500'
}, {
  label: 'これまでの経歴',
  icon: 'i-ic-baseline-work-history',
  color: 'text-cyan-500'
}, {
  label: 'SNS',
  icon: 'i-codicon-github-project',
  color: 'text-cyan-500'
}]
</script>

<template>
  <UVerticalNavigation :links="links" :ui="{ wrapper: 'truncate' }">
    <template #icon="{ link }">
      <UIcon :name="link.icon" :class="link.color" class="text-base" />
    </template>
  </UVerticalNavigation>
</template>