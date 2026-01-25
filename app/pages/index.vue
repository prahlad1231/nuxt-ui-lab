<script setup lang="ts">
import type { NavigationMenuItem } from "@nuxt/ui";

const items: NavigationMenuItem[][] = [
  [
    {
      label: "Dashboard",
      icon: "i-lucide-layout-dashboard",
    },
    {
      label: "About",
      icon: "i-lucide-info",
    },
    {
      label: "Components",
      icon: "i-lucide-component",
      children: [
        {
          label: "Buttons",
          icon: "i-lucide-square-arrow-right",
        },
        {
          label: "Cards",
          icon: "i-lucide-id-card",
        },
      ],
    },
  ],
  [
    {
      label: "Settings",
      icon: "i-lucide-settings",
    },
  ],
];
</script>

<template>
  <UDashboardGroup>
    <UDashboardSidebar collapsible resizable>
      <UNavigationMenu :items="items[0]" orientation="vertical" />
      <UNavigationMenu
        :items="items[1]"
        orientation="vertical"
        class="mt-auto"
      />
    </UDashboardSidebar>
    <slot />
  </UDashboardGroup>
</template>
