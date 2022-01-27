<template>
  <div>
    <MenuButton
      class="inline-flex justify-center w-full px-4 py-2 text-sm font-medium text-white bg-black rounded-md bg-opacity-20 hover:bg-opacity-30 focus:outline-none focus-visible:ring-2 focus-visible:ring-white focus-visible:ring-opacity-75"
      v-slot="{ open }"
    >
      <slot />
      <Icon
        :name="open ? 'chevron-up' : 'chevron-down'"
        class="w-5 h-5 ml-2 -mr-1 text-violet-200 hover:text-violet-100"
        aria-hidden="true"
      />
    </MenuButton>
  </div>
</template>

<script setup>
import Icon from 'vue-heroicon-next'
import { MenuButton } from '@headlessui/vue'
</script>

