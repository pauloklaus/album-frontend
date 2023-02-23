<script setup lang="ts">
import { RouterLink, RouterView } from "vue-router";
import LoginView from "@/views/LoginView.vue";
</script>

<template>
  <LoginView v-if="true" />

  <template v-else>
    <header>
      <nav>
        <RouterLink to="/">Home</RouterLink>
        <RouterLink to="/about">About</RouterLink>
      </nav>
    </header>

    <RouterView />
  </template>
</template>
