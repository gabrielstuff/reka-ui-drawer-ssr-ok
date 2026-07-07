<script setup lang="ts">
import { DrawerContent, DrawerOverlay, DrawerPortal, DrawerRoot, DrawerTrigger } from 'reka-ui'
</script>

<template>
  <DrawerRoot :default-open="true">
    <DrawerTrigger>Open</DrawerTrigger>
    <DrawerPortal force-mount>
      <DrawerOverlay />
      <DrawerContent>Hello from reka-ui</DrawerContent>
    </DrawerPortal>
  </DrawerRoot>
</template>
