<script>
  let isActive = false;
  const toggle = () => {
    isActive = !isActive;
  }
</script>

<button on:click={toggle} class="toggler {isActive ? "active" : ""}">
  <div class="toggle {isActive ? "active" : ""}"></div>
</button>

<style>
  * {
    font-family: 'Inter', sans-serif;
    color: #132B50
  }
    
  .toggler {
    width: 60px;
    height: 36px;
    border: 1px solid #132B50;
    background-color: white;
    border-radius: 44px;
    display: flex;
    align-items: center;
    justify-content: start;
    padding: 6px;
    cursor: pointer;
    transition: all ease-in 0.4s;
  }

  .toggler.active {
    background-color: #132B50;
  }

  .toggle {
    position: relative;
    width: 22px;
    height: 22px;
    background-color: #132B50;
    border-radius: 40px;
    transition: all ease-in 0.3s;
  }

  .toggle.active {
    transform: translateX(25px);
    background-color: white;
  }
</style>