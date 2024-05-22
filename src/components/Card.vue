<template>
    <q-card class="card-container">
      <q-img :src="image" :alt="title" class="card-image">
        <q-card-section class="card-section">
          <div class="text-h6">{{ title }}</div>
          <div>{{ description }}</div>
        </q-card-section>
  
        <q-card-actions class="card-actions">
          <q-btn flat @click="$emit('view-details')">View Details</q-btn>
        </q-card-actions>
      </q-img>
    </q-card>
  </template>
  
  <script>
  export default {
    name: 'Card',
    props: {
      title: {
        type: String,
        required: true
      },
      description: {
        type: String,
        required: true
      },
      image: {
        type: String,
        required: true
      }
    }
  }
  </script>
  
  <style scoped>
  .card-container {
    width: 100%;
  }
  
  .card-image {
    width: 100%;
    height: 30%; 
    object-fit: cover;
    position: relative;
    overflow: hidden;
  }
  
  .card-section {
    position: absolute;
    bottom: 0;
    left: 0;
    right: 0;
    background: rgba(0, 0, 0, 0.5);
    color: white;
    padding: 1rem;
  }
  
  .card-actions {
    position: absolute;
    bottom: 1rem;
    right: 1rem;
  }
  </style>
  