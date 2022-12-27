<script setup>
  // You might choose this based on an API call or logged-in status
  const layout = 'default'
</script>
<template>
  <div>
    <nav>
      <NuxtLink to="/">Home</NuxtLink>
      <NuxtLink to="/test/">Test</NuxtLink>
    </nav>
    <NuxtErrorBoundary @error="someErrorLogger">
      <!-- You use the default slot to render your content -->
      <template #error="{ error }">
        You can display the error locally here.
        <button @click="error = null">This will clear the error.</button>
      </template>
    </NuxtErrorBoundary>
    <NuxtLayout :name="layout">
      <NuxtPage />
    </NuxtLayout>
  </div>
</template>
