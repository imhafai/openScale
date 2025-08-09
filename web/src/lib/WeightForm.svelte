<script>
  let weight = '';
  let entries = [];

  function addEntry() {
    if (weight.trim() === '') return;
    entries = [...entries, { value: parseFloat(weight), date: new Date() }];
    weight = '';
  }
</script>

<div>
  <label>
    Weight (kg):
    <input type="number" bind:value={weight} step="0.1" />
  </label>
  <button on:click={addEntry}>Add</button>
</div>

{#if entries.length}
  <h2>Entries</h2>
  <ul>
    {#each entries as entry}
      <li>{entry.date.toLocaleString()}: {entry.value} kg</li>
    {/each}
  </ul>
{/if}

<style>
  div {
    margin-bottom: 1rem;
  }
  input {
    margin-right: 0.5rem;
  }
</style>
