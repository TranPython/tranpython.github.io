<template>
  <div>
    <h2 class="uppercase text-xs font-semibold text-gray-400 mb-4">FIND ME ON</h2>
    <div class="space-y-5">
      <NuxtLink
        v-for="link in links"
        :key="link.icon"
        :to="link.url"
        target="_blank"
        external
        class="flex items-end gap-4 dark:hover:text-gray-300 group"
      >
        <span class="text-sm">
          {{ link.name }}
        </span>
        <div
          class="flex-1 border-b border-dashed border-gray-300 dark:border-gray-800 group-hover:border-gray-700"
        ></div>
        <Icon :name="link.icon" class="w-6 h-6"></Icon>
      </NuxtLink>
    </div>
  </div>
</template>

<script lang="ts" setup>
const links = [
  {
    name: "Twitter",
    url: "https://twitter.com/tranpython",
    icon: "mdi:twitter",
  },
  {
    name: "GitHub",
    url: "https://github.com/tranpython",
    icon: "mdi:github",
  },
  {
    name: "Linkedin",
    url: "hhttps://www.linkedin.com/in/tranpython",
    icon: "mdi:linkedin",
  },
  {
    name: "Telegram",
    url: "https://t.me/tranpython",
    icon: "mdi:telegram",
  },
  {
    name: "Slack",
    url: "https://join.slack.com/t/tranpython/shared_invite/zt-2c067f2d3-NJEruR2tp0U4d58U20sxpQ",
    icon: "mdi:slack",
  },
];
</script>
