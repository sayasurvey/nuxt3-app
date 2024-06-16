<template>
  <div style="height: 100vh;">
    <vue-pdf-app :pdf="pdfPath"></vue-pdf-app>
  </div>
</template>

<script setup>
import { ref } from 'vue';
import VuePdfApp from 'vue3-pdf-app';
import 'vue3-pdf-app/dist/icons/main.css';

// Correct path without '/public'
const pdfPath = ref('/materials006_nuri1.pdf');
</script>

<script>
export default {
  components: {
    VuePdfApp
  }
};
</script>