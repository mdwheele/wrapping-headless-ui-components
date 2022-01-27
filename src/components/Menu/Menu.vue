<template>
  <div class="w-56 text-right">
    <Menu as="div" class="relative inline-block text-left">
      <slot />
    </Menu>
  </div>
</template>

<script setup>
import { Menu } from '@headlessui/vue'
</script>
