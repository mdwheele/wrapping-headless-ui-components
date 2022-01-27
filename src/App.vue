<script setup>
  import { Menu, MenuItem, MenuItems, MenuButton } from './components/Menu'

  function onClick(e) {
    window.alert(`The "${e.target.innerText}" menu item was selected.`)
  }
</script>

<template>
  <div class="h-screen flex flex-col justify-center items-center font-sans bg-gradient-to-r from-purple-500 to-indigo-500">
    <Menu>
      <MenuButton>Options</MenuButton>
      <MenuItems>
        <div class="p-1">
          <MenuItem @click="onClick" icon="pencil">Edit</MenuItem>
          <MenuItem @click="onClick" icon="document-duplicate">Duplicate</MenuItem>
          <MenuItem @click="onClick" icon="cursor-click">Move</MenuItem>
        </div>
        <div class="p-1">
          <MenuItem @click="onClick" icon="archive">Archive</MenuItem>
          <MenuItem @click="onClick" icon="trash">Delete</MenuItem>
        </div>
      </MenuItems>
    </Menu>
  </div>  
</template>