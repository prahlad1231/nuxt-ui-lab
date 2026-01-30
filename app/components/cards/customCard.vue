<script setup lang="ts">
const { variant, title, description, footer } = defineProps<{
  variant?: "solid" | "soft" | "outline" | "subtle";
  title?: string;
  description?: string;
  footer?: string;
}>();
</script>
<template>
  <UCard :variant="variant">
    <template #header>
      <h1>{{ title }}</h1>
    </template>
    <div>
      <p>{{ description }}</p>
    </div>
    <template #footer>
      <div>
        <h3>{{ footer }}</h3>
      </div>
    </template>
  </UCard>
</template>
