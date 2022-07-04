<script>
  import Login from "./lib/Login/Login.svelte";
</script>

<main>
  <div class="carousel">
    <Login />
  </div>
</main>

<style>
  :global(*) {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
  }

  :global(body) {
    width: 100vw;
    height: 100vh;
  }

  main {
    display: grid;
    align-items: center;
    height: 100vh;
    width: 100%;
    background-color: rgb(209, 209, 209);
  }

  .carousel {
    display: flex;
    justify-content: center;
    align-items: center;
  }
</style>
