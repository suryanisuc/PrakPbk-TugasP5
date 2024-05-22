<template>
    <q-footer class="footer-background">
      <q-toolbar>
        <q-toolbar-title>{{ footerText }}</q-toolbar-title>
      </q-toolbar>
      <div class="footer-content">
        <div class="footer-section">
          <q-icon name="location_on" /> Jl. Marpoyan Damai,Pekanbaru, Indonesia
        </div>
        <div class="footer-section">
          <q-icon name="email" /> Sucistore@gmail.co.id
        </div>
        <div class="footer-section">
          <q-icon name="info" /> © 2024 Suci Store
        </div>
      </div>
    </q-footer>
  </template>
  
  <script>
  export default {
    name: 'Footer',
    props: {
      footerText: {
        type: String,
        required: true
      }
    }
  }
  </script>
  
  <style scoped>
  .footer-background {
    background-color: #cccccc;
  }
  
  .footer-content {
    display: flex;
    justify-content: space-around;
    align-items: center;
    height: 100%; 
  }
  
  .footer-section {
    display: flex;
    align-items: center;
    color: black;
    margin-bottom: 30px;
  }
  </style>
  