<template>
  <navbar />
  <router-view></router-view>
</template>

<script lang="ts">
import Navbar from "./components/Navbar.vue";
export default {
  name: "App",
  components: {
    Navbar,
  },
};
</script>