<script>
  import Toggler from './Toggler.svelte';

  export let disableContinue;

</script>

<article class="action-bar">
  <span class="stay-signed-in">
    <Toggler />
    <p class="stay-signed-in-text">Stay signed in</p>
  </span>
  
  <button 
      
      class="continue-btn {disableContinue ? "disabled":""}">
    Continue</button>
</article>


<style>
  .action-bar {
    max-width: 371px;
    display: flex;
    justify-content: space-between;
  }

  .stay-signed-in {
    display: flex;
    align-items: center;
  }

  .stay-signed-in-text {
    margin-left: 8px;
    font-weight: 600;
  }

  .continue-btn {
    padding: 16px;
    color: white;
    background-color: #132B50;
    border: 0;
    border-radius: 8px;
    font-weight: 600;
    font-size: 16px;
    cursor: pointer;
    transition: all ease-in 0.15s;
  }

  .continue-btn.disabled {
    background-color: gray;
    cursor: not-allowed;
  }

  .continue-btn:not(.disabled):hover {
    background-color: hsl(216, 62%, 30%);
  }

  .continue-btn:not(.disabled):active {
    position: relative;
    top: 1px;
  }
  
</style>