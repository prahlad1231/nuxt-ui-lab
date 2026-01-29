<script setup lang="ts">
import CustomButton from "~/components/customButton.vue";

definePageMeta({
  layout: "dashboard",
});
</script>

<template>
  <UDashboardNavbar title="Buttons" />
  <div class="p-6">
    <CustomButton />
  </div>
</template>
