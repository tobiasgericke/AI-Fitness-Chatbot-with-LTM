<template>
    <div class="notes-list">
      <h3>Long Term Memory:</h3>
      <ul>
        <li v-for="(note, index) in notes" :key="index">{{note}}</li>
      </ul>
    </div>
  </template>
  
  <script setup>
  import { ref } from 'vue';
  
  const notes = ref(['Note 1', 'Note 2', 'Note 3']); //Replace with actual data
  </script>