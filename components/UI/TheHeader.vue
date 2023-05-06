<template>
  <header class="flex flex-col gap-4 md:flex-row justify-between items-center py-10">
      <nuxt-link to="/" class="text-3xl font-bold border-b-2 border-green-500"><span class="text-green-500">Nuxt</span>Movies</nuxt-link>
      <SearchMovie />
  </header>
</template>

<script>
export default {
    name: 'TheHeader',
    
    

}
</script>

<style>

</style>
