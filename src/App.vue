<script setup>
import { RouterLink, RouterView } from 'vue-router'
import Branding from './components/Branding.vue'
</script>

<template>
  <header>
    <Branding name="Drive" />
    <nav>
      <RouterLink to="/">My Drive</RouterLink>
      <RouterLink to="/star">Starred</RouterLink>
      <RouterLink to="/trash">Trash</RouterLink>
      <RouterLink to="/about">About</RouterLink>
    </nav>
    <div>
      <p style="text-align: center">Source:<a href="">Github</a></p>
    </div>
  </header>

  <RouterView />
</template>

<style scoped>
header {
  --nav-color-active: rgb(0, 189, 126);
  --nav-color-inactive: rgb(0, 189, 126);
  --nav-color-bg-active: brown;
  --nav-color-bg-inactive: blue;
  --nav-border: white;
}
header {
  width: 300px;
  padding-right: 30px;
  height: 100vh;
}
#Navbar {
  display: flex;
  flex-direction: column;
  justify-items: flex-end;
}
nav {
  width: 100%;
  display: flex;
  flex-direction: column;
  gap: 3px;
  font-size: 30px;
  text-align: center;
  margin-top: 2rem;
}

nav a.router-link-exact-active {
  color: var(--nav-color-active);
  background-color: var(--nav-color-bg-active);
  border-left: 0px;
  border-left: 5px solid var(--nav-border);
}

nav a.router-link-exact-active:hover {
  background-color: transparent;
}

nav a {
  display: inline-block;
  color: var(--nav-color-inactive);
  background-color: var(--nav-color-bg-inactive);
  border-radius: 0 50px 50px 0;
}
</style>
