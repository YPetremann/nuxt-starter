<script setup>
  const { data: plop } = await useFetch('/api/test')
</script>

<template>
  <pre>{{ plop }}</pre>
</template>
