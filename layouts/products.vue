<template>
  <div class="bg-white dark:bg-gray-800">
    <header class="shadow-sm bg-white dark:bg-gray-800">
      <nav class="container mx-auto p-4 text-gray-900 dark:text-white">
        <NuxtLink to="/products" class="font-bold">Merch</NuxtLink>
      </nav>
    </header>
    <div class="container mx-auto p-4">
      <slot />
    </div>
    <footer class="container mx-auto p-4 flex justify-between border-t-2">
      <ul class="flex gap-4 text-gray-900 dark:text-white">
        <li><NuxtLink to="/">Home</NuxtLink></li>
        <li><NuxtLink to="/currencyapi">Currency Api</NuxtLink></li>
        <li><NuxtLink to="/products">Merch</NuxtLink></li>
      </ul>
    </footer>
  </div>
</template>

<style scoped>
.router-link-exact-active {
  color: aqua;
}
</style>
