<template>
  <v-app-bar color="primary" density="compact" dark>

    <!-- Logo or Brand Name -->
    <v-app-bar-title>My App</v-app-bar-title>

    <!-- Spacer for aligning the menu on the right -->
    <v-spacer></v-spacer>

    <!-- Desktop Menu -->
    <div class="d-none d-md-flex justify-center items-center">
      <v-btn text to="/">Home</v-btn>
      <v-btn text to="/about">About</v-btn>
      <v-btn text to="/contact">Contact</v-btn>
    </div>


    <!-- Mobile Menu -->
    <v-app-bar-nav-icon @click="toggleDrawer"></v-app-bar-nav-icon>
      <v-navigation-drawer
        v-model="drawer"
        :location="$vuetify.display.mobile ? 'bottom' : undefined"
        temporary
      >
        <v-list
          :items="items"
        ></v-list>
      </v-navigation-drawer>

          </v-app-bar>
</template>

<script setup>
import { ref, watch } from "vue";

const items = [
  { title: "Home", value: "/" },
  { title: "About", value: "/about" },
  { title: "Contact", value: "/contact" },
];

const drawer = ref(false);
const group = ref(null);

// Automatically close drawer on group change (if applicable)
watch(group, () => {
  drawer.value = false;
});

function toggleDrawer() {
  console.log("Drawer state before:", this.drawer);
  this.drawer = !this.drawer;
  console.log("Drawer state after:", this.drawer);
}

</script>