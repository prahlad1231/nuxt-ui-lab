<script setup lang="ts">
import type { NavigationMenuItem } from "@nuxt/ui";

const items: NavigationMenuItem[][] = [
  [
    {
      label: "Dashboard",
      icon: "i-lucide-layout-dashboard",
      to: "/",
    },
    {
      label: "About",
      icon: "i-lucide-info",
      to: "/about",
    },
    {
      label: "Components",
      icon: "i-lucide-component",
      children: [
        {
          label: "Buttons",
          icon: "i-lucide-square-arrow-right",
          to: "/components/buttons",
        },
        {
          label: "Cards",
          icon: "i-lucide-id-card",
          to: "/components/cards",
        },
      ],
    },
  ],
  [
    {
      label: "Settings",
      icon: "i-lucide-settings",
      to: "/settings",
    },
    {
      label: "Profile",
      icon: "i-lucide-user",
      to: "/profile",
    },
  ],
];

const route = useRoute();
const title = computed(() => route.meta?.title || "Dashboard");
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

    <UDashboardPanel>
      <slot />
    </UDashboardPanel>
  </UDashboardGroup>
</template>
