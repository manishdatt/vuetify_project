<template>
  <v-app-bar scroll-behavior="hide" color="#FFF999" density="prominent" dark>

    <!-- Logo or Brand Name 
        <v-app-bar-title>My App</v-app-bar-title>
    -->
    <v-row>
      <v-col cols="2">
      <div class="d-flex align-center">
        <v-img src="@/assets/logo.png" class="ma-10" alt="Logo" max-height="50" max-width="50"></v-img>
      </div>
      </v-col>
      <v-col cols="8">
      <div class="justify-center items-center" style="flex: 1;">
        <div class="justify-center items-center" style="display: flex; justify-content: center; align-items: center;">
        <h1 class="py-6 tektur-400">Welcome!</h1>
        </div>
        <div class="justify-center items-center tektur-400" style="display: flex; justify-content: center; align-items: center;">
        <v-btn text to="/">Home</v-btn>
        <v-btn text to="/about">About</v-btn>
        <v-btn text to="/contact">Contact</v-btn>
        </div>
      </div>
      </v-col>
    </v-row>

          </v-app-bar>
</template>

<script setup>
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Tektur:wght@400..900&display=swap');

.tektur-400 {
  font-family: "Tektur", sans-serif;
  font-optical-sizing: auto;
  font-weight: 400;
  font-style: normal;
  font-variation-settings:
    "wdth" 100;
}
</style>