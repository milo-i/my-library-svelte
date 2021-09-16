<script>
  export let movie;
</script>

<div>
  Name: {movie.movie_name}<br />
  Color: {movie.movie_color}<br />
  Color: {movie.movie_genres}<br />
  <img src={movie.movie_pic} alt="represents the movie" />
</div>

<style>
  div {
    margin: 0 auto;
    padding: 10px;
    max-width: 400px;
    border: 1px solid black;
    align-items: center;
    margin-bottom: 30px;
  }
</style>
