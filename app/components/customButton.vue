<script setup lang="ts">
const toast = useToast();

function buttonClicked(description: string) {
  toast.add({
    title: "Clicked!",
    description: description,
    icon: "i-lucide-mouse-pointer-click",
  });
}
</script>

<template>
  <div class="p-6 flex gap-2">
    <UButton @click="buttonClicked('Button Clicked')">Button</UButton>
    <UButton loading>Loading Button</UButton>
    <UButton
      icon="i-lucide-rocket"
      size="lg"
      variant="subtle"
      @click="buttonClicked('Icon Subtle Clicked')"
      >Icon Subtle</UButton
    >
    <UButton
      trailing-icon="i-lucide-arrow-right"
      @click="buttonClicked('Trailing Icon Clicked')"
      >Trailing Icon</UButton
    >
  </div>
</template>
