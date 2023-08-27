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
  <div class="greetings">
    <h1 class="green">{{ name }}</h1>
  </div>
</template>

<style scoped></style>
