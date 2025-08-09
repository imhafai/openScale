<script>
  import WeightForm from './lib/WeightForm.svelte';
</script>

<main>
  <h1>openScale Web PoC</h1>
  <p>Record your weight entries below. Data is stored locally in this demo.</p>
  <WeightForm />
</main>

<style>
  main {
    max-width: 600px;
    margin: 0 auto;
    padding: 1rem;
    font-family: system-ui, sans-serif;
  }
  h1 {
    text-align: center;
  }
</style>
