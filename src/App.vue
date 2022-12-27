<script setup>
import { RouterLink, RouterView } from 'vue-router'
</script>

<template>
  <header>
    <div class="wrapper mx-auto">
      <nav class="navbar navbar-expand-lg navbar-dark bg-primary">
        <div class="container">
          <div class="collapse navbar-collapse" id="navbarNav">
            <ul class="navbar-nav" style="margin-left: 38%;">
              <li class="nav-item">
                <RouterLink to="/" class="nav-link">Home</RouterLink>
              </li>
              <li class="nav-item">
                <RouterLink to="/notebooks" class="nav-link">Notebooks</RouterLink>
              </li>
              <li class="nav-item">
                <RouterLink to="/socmeds" class="nav-link">Contact Us</RouterLink>
              </li>
            </ul>
            
            </div>
        </div>
    </nav>
    </div>
  </header>
  <RouterView />
</template>

<style scoped>

</style>
