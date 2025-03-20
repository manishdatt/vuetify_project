<template>
  <v-app-bar scroll-behavior="hide" color="primary" density="compact" dark>
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
    <v-app-bar-nav-icon class="d-md-none" @click="drawer = !drawer"></v-app-bar-nav-icon>

    <!-- Navigation Drawer for Mobile -->
    <v-navigation-drawer v-model="drawer" app temporary>
      <v-list>
        <v-list-item-group>
          <v-list-item>
            <v-list-item-title>Home</v-list-item-title>
          </v-list-item>
          <v-list-item>
            <v-list-item-title @click="$router.push('/about')">About</v-list-item-title>
          </v-list-item>
          <v-list-item>
            <v-list-item-title>Contact</v-list-item-title>
          </v-list-item>
        </v-list-item-group>
      </v-list>
    </v-navigation-drawer>
  </v-app-bar>
</template>

<script>
export default {
  data() {
    return {
      drawer: false, // For toggling the mobile navigation drawer
    };
  },
};
</script>
