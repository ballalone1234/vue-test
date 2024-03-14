<script setup>
import { ref, computed } from 'vue'
import NotFound from './views/NotFound.vue'
import Navbar from "@/components/Navbar.vue";

</script>

<template>
  <div>
  </div>
  <Navbar v-show="!isLogin" />
  <div id="content">
  <router-view />
  </div>
</template>