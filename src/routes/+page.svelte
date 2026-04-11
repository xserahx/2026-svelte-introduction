<script>
  import Canvas from '$lib/components/Canvas.svelte';
  import ClicksCounter from '$lib/components/ClicksCounter.svelte';
  let count = $state(5);

  $inspect(count);
</script>

<h1>Welcome to SvelteKit</h1>
<p>Visit <a href="https://svelte.dev/docs/kit">svelte.dev/docs/kit</a> to read the documentation</p>

<ClicksCounter bind:initialCount = {count} />

{#if count > 10 && count < 20}
  <p> count from parent is {count} </p>
{:else if count > 30}
  <p> wow! That's a lot of clicks!</p>
{:else}
  <p> count is not in range </p>
{/if} 

<Canvas />
<style>
  h1 {
   color: deepskyblue;
  }
</style>
