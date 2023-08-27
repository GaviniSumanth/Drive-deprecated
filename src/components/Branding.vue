<script setup>
defineProps({
  name: {
    type: String,
    default: 'name',
    required: true
  }
})
</script>

<template>
  <div id="branding">
    <img alt="Vue logo" id="logo" src="@/assets/logo.svg" width="125" height="125" />
    <h1 class="green">{{ name }}</h1>
  </div>
</template>

<style scoped>
#branding {
  display: flex;
  align-items: center;
  width: 100%;
}
#logo {
  height: inherit;
  width: 50px;
  margin-right: 10px;
}
</style>
