<template>
  <section id="api" class="api">
    <div class="row mt-md-5 mt-sm-5 mt-xs-5">
      <div class="col-lg-6 col-xs-12" v-for="(movie, index) of movies" :key="index">
        <div class="d-flex justify-content-center align-center">
          <div class="column justify-content-center">
            <div class="p-3 justify-content-center">
              <img :src="movie.Poster" alt="movie poster" />
            </div>

            <div class="column justify-content-center">
              <h3>Título: {{ movie.Title }}</h3>
              <br />
              <h3>Año: {{ movie.Year }}</h3>
              <br />
              <h3>Tipo: {{ movie.Type }}</h3>
            </div>
          </div>
        </div>
        <div class="d-flex container-fluid justify-content-end pb-2 mt-n2">
          <a
            :href="'https://www.imdb.com/title/' + movie.imdbID"
            target="_blank"
            class="btn btn-outline-info"
          >
            Info
          </a>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
import axios from "axios";

export default {
  name: "SectionApi",
  data() {
    return {
      movies: null,
    };
  },
  mounted() {
    axios
      .get("http://www.omdbapi.com/?s=energy&type=movie&apikey=23daade9")
      .then((response) => {
        this.movies = response.data.Search.slice(0, 4);
        console.log(this.movies);
      });
  },
};
</script>