<template>
  <q-layout view="hHh lpR fFf">
    <q-header elevated class="bg-dark text-white">
      <q-toolbar>
        <q-toolbar-title> Nuxt3 Playground </q-toolbar-title>
        <q-btn stretch flat :label="$t('home')" to="/" />
        <q-separator dark vertical />
        <q-btn stretch flat :label="$t('about')" to="/about" />
      </q-toolbar>
    </q-header>
    <q-page-container :style="pageContainerStyle">
      <slot></slot>
    </q-page-container>
  </q-layout>
</template>

<script setup lang="ts">
const pageContainerStyle = computed(() => ({
  maxWidth: '1080px',
  margin: '0 auto',
}));
</script>
