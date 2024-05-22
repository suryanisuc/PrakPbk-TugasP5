<template>
    <q-header elevated class="pink-background">
      <q-toolbar>
        <q-btn flat dense round icon="menu" aria-label="Menu" @click="$emit('toggle-left-drawer')" />
        <q-toolbar-title>
          {{ title }}
        </q-toolbar-title>
      </q-toolbar>
    </q-header>
  </template>
  
  <script>
  export default {
    name: 'Navbar',
    props: {
      title: {
        type: String,
        required: true
      }
    }
  }
  </script>
  
  <style scoped>
  .pink-background {
    background-color: #ff69b4; /* Ganti dengan kode warna pink yang Anda inginkan */
  }
  </style>
  