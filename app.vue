<template>
  <vue-pdf-app style="height: 100vh;" pdf="https://drive.google.com/file/d/1V35ETdOd-fkgzP-v4lxulb_Tk4L7m7vU/view?usp=sharing"></vue-pdf-app>
</template>

<script>
import VuePdfApp from "vue3-pdf-app";
import "vue3-pdf-app/dist/icons/main.css";

export default {
  components: {
    VuePdfApp
  }
};
</script>