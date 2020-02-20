<script>
  import SvelteScrollShadow from "../lib/index.svelte";
</script>

<style>
  main {
    align-items: center;
    display: flex;
    flex-flow: column wrap;
    justify-content: center;
    width: 100%;
  }

  div {
    align-items: center;
    background-color: #417b5a;
    display: flex;
    flex-flow: column wrap;
    height: 120px;
    justify-content: center;
    margin: 10px;
    width: 300px;
  }

  h1 {
    color: #1f2041;
    text-transform: uppercase;
  }
</style>

<main>
  <h1>Svelte Scroll Shadow</h1>
  <SvelteScrollShadow let:onRequest let:onExit>
    <div>
      <button on:click={() => onRequest()}>FullScreen</button>
      <button on:click={() => onExit()}>Screen</button>
    </div>
  </SvelteScrollShadow>
</main>
