<template>
  <div class="flex w-1/2">

        <input @keyup.prevent="searchedMovies" v-model="searchText" type="text" name="search" id="search" placeholder="Search for movie" class="w-full bg-white p-2 focus:outline-none rounded-lg shadow-md">
  </div>
</template>

<script>
export default {
    name: 'SearchMovies',
    data() {
        return {
            searchText: ''
        }
    },
    computed: {
        movies() {
            return this.$store.state.movies
        }
    },

    methods: {
        searchedMovies() {
            if(this.searchText) {
                return this.$store.dispatch('searchMovies', this.searchText)
            } else {
                this.searchText = '';
                return this.$store.state.movies;
            }
            
        }
    },

    // created() {
    //     this.searchedMovies();
    // }
}
</script>

<style>

</style>
