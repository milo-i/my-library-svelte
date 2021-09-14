<script>
  import { onMount } from 'svelte';
  import Film from './Film.svelte';

  export let movies = [];

  onMount(() => {
    fetch('http://localhost:3000/movies')
      .then((res) => res.json())
      .then((data) => {
        console.log(data);

        movies = data;
      });
  });
</script>

<div>
  {#each movies as movie}
    <div><Film {movie} /></div>
  {:else}
    <div>Hämtar filmer...</div>
  {/each}
</div>

<style></style>
