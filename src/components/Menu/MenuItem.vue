<template>
  <MenuItem v-slot="{ active }">
    <button 
      :class="[
        'group flex rounded-md items-center w-full px-2 py-2 text-sm',
        active ? 'bg-violet-500 text-white' : 'text-gray-900',
      ]"
    >
      <Icon
        :name="icon"
        :active="active"
        outline
        class="w-5 h-5 mr-2"
        aria-hidden="true"
      />
      <slot />
    </button>
  </MenuItem>
</template>

<script setup>
import { MenuItem } from '@headlessui/vue'
import Icon from 'vue-heroicon-next'

const props = defineProps({
  icon: {
    type: String,
    required: false
  }
})
</script>
