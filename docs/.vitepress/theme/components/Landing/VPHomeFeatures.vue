<script setup lang="ts">
import { useData } from 'vitepress'
import VPFeatures from 'vitepress/dist/client/theme-default/components/VPFeatures.vue'

const { frontmatter: fm } = useData()
</script>

<template>
  <VPFeatures
    v-if="fm.features"
    class="VPHomeFeatures"
    :features="fm.features"
  />
</template>