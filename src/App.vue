<script setup lang="ts">
import { RouterLink, RouterView } from "vue-router";
</script>

<template>
  <header :class="$style.parent">
    <nav :class="$style.nav">
      <RouterLink to="/">Home</RouterLink>
      <RouterLink to="/page-not-found">Page Not Found</RouterLink>
    </nav>
  </header>

  <RouterView />
</template>

<style module lang="scss">
.parent {
  padding-bottom: 24px;
  border-bottom: 2px solid gray;

  .nav {
    display: flex;
    justify-content: center;

    & > a {
      margin-right: 16px;
      font-size: 24px;

      &:last-child {
        margin-right: 0;
      }
    }
  }
}
</style>
