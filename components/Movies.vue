<template>
  <div>
      <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 xl:grid-cols-4 gap-4" v-if="movies.length > 0">
        <Movie v-for="(movie, index) in movies" :key="index" class="" :movie=movie />
        <!-- :movie=movie  is our props which passed to Movie component--> 
      </div>
      <div v-else class="text-center text-2xl mx-auto font-bold">No movies to show</div>
  </div>
</template>

<script>
export default {
    computed: {
    movies() {
      return this.$store.state.movies;
    }
  },

  mounted() {
    this.$store.dispatch('getAllMovies');
  }
    
}
</script>

<style>

</style>
