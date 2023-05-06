<template>
    <div class="">
      <div class="movie_card relative overflow-hidden transition">
        <img :src="`https://image.tmdb.org/t/p/w500/${movie.poster_path ? movie.poster_path : 'https://via.placeholder.com/500'}`" alt="" class="object-cover movie_img">
        <p v-if="movie.vote_average" class="absolute top-0 left-0 px-4 py-2 bg-red-500 text-white font-bold">{{movie.vote_average}}</p>
        <div id="movie_details" class="w-full p-2 text-white absolute bottom-0 bg-red-500 leading-normal transition ease-in-out duration-30 all">

          <h4 class="font-bold">Movie Name: {{movie.title}}</h4>
          <p class="font-medium">Overview: <span class="text-gray-200">{{ movie.overview.slice(0, 200) }}</span> </p>
          <small class="font-regular italic">Release Date: {{movie.release_date}}</small>
        </div>   
      </div>
    </div>
</template>

<script>

export default {
  props: ['movie'],

  
}
</script>

<style>
  .movie_card:hover #movie_details {
      transform: translateY(0);
  }

  #movie_details {
    transform: translateY(100%);
  }

</style>
