<script>
  export let movieTitle;
  export let movieColor;
  export let movieGenre;

  const handleSubmit = () => {
    console.log(movieTitle);

    const addMovie = {
      movieTitle,
      movieGenre,
      movieColor,
    };

    fetch('http://localhost:3000/movies', {
      method: 'post',
      headers: {
        'Content-type': 'application/json',
      },
      body: JSON.stringify(addMovie),
    })
      .then((res) => res.json())
      .then((data) => console.log(data))
      .catch((err) => console.log('error', err));
    // console.log(movieTitle, movieColor, movieGenre);
  };
</script>

<form on:submit|preventDefault={handleSubmit}>
  <input type="text" placeholder="Filmtitel" bind:value={movieTitle} />
  <input type="text" placeholder="Genre" bind:value={movieGenre} />
  <input type="text" placeholder="Filmfärg" bind:value={movieColor} />
  <button>Lägg till film</button>
</form>

<style>
</style>
