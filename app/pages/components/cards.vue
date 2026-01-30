<script setup lang="ts">
import CustomCard from "~/components/cards/customCard.vue";

definePageMeta({
  layout: "dashboard",
});
</script>

<template>
  <UDashboardNavbar title="Cards Demo" />
  <div class="p-6 gap-2 flex">
    <CustomCard
      title="Default Card"
      description="This is a normal/outline card"
      footer="Footer"
    />
    <CustomCard
      variant="subtle"
      title="Subtle Card"
      description="This is a subtle card"
      footer="Footer"
    />
    <CustomCard
      variant="solid"
      title="Solid Card"
      description="This is a solid card"
      footer="Footer"
    />
    <CustomCard
      variant="soft"
      title="Soft Card"
      description="This is a soft card"
      footer="Footer"
    />
  </div>
</template>
