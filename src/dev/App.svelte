<script>
  import ScrollShadow from '../lib/ScrollShadow.svelte';
  import cars from './cars.js';
</script>

<style>
  main {
    display: flex;
    width: 100%;
    height: 100%;
    align-items: center;
    justify-content: center;
    flex-direction: column;
  }

  h1 {
    color: white;
    text-shadow: 1px 1px 2px black;
    margin: 0;
  }

  h5 {
    color: #333;
    font-size: 20px;
    font-weight: bold;
    margin: 10px 0px;
    text-align: center;
  }

  h4 {
    color: white;
    margin: 10px 0px;
    margin-bottom: 40px;
  }

  .root {
    display: flex;
    justify-content: center;
  }

  .card {
    box-shadow: 0px 1px 3px 0px rgba(0, 0, 0, 0.2),
      0px 1px 1px 0px rgba(0, 0, 0, 0.14), 0px 2px 1px -1px rgba(0, 0, 0, 0.12);
    display: flex;
    flex-direction: column;
    border-radius: 2px;
    width: 500px;
    max-width: 40%;
    background-color: white;
    max-height: 400px;
  }

  .card:first-child {
    margin-right: 30px;
  }

  .card:last-child {
    margin-right: 0px;
  }

  ul {
    list-style: none;
    border-radius: 2px;
    padding: 0px;
    margin: 0px;
  }

  li {
    padding: 15px;
    color: #333;
  }

  li:hover {
    background-color: #eeeeee;
  }
</style>

<main>
  <h1>Svelte Scroll Shadow</h1>
  <h4>
    Component that customizes the image and inserts shadow when scrolling exists
  </h4>
  <div class="root">
    <div class="card">
      <h5>With SvelteScrollShadow</h5>
      <ScrollShadow isShadow={true} scrollWidth="10px" scrollPadding="5px">
        <ul>
          {#each cars as language}
            <li>{language}</li>
          {/each}
        </ul>
      </ScrollShadow>
    </div>
    <div class="card">
      <h5>Without SvelteScrollShadow</h5>
      <ul style="overflow-y:scroll">
        {#each cars as language}
          <li>{language}</li>
        {/each}
      </ul>
    </div>
  </div>
</main>
