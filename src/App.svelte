<script>
  import Bibliotek from './Bibliotek.svelte';
  import Form from './Form.svelte';

  let movies = 'Mitt filmbibliotek';
</script>

<main>
  <h1>{movies}!</h1>
  <Form />
  <Bibliotek />
</main>

<style>
  main {
    text-align: center;
    padding: 1em;
    max-width: 240px;
    margin: 0 auto;
  }

  h1 {
    color: gray;
    text-transform: uppercase;
    font-size: 4em;
    font-weight: 100;
  }

  @media (min-width: 640px) {
    main {
      max-width: none;
    }
  }
</style>
