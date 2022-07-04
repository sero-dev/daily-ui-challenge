<svelte:head>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@500;600;700&display=swap" rel="stylesheet">
</svelte:head>

<script>
  export let password;
  let showPassword = false;

  const toggleVisibility = () => {
    showPassword = !showPassword;
  }

  const onPasswordChange = (e) => {
    password = e.target.value;
  }

</script>

<article class="password-form">
  <label class="input-label" for="password">Password</label>
  <div class="input-container">
    <div class="password-input">
      <img class="input-icon" src="./assets/lock.svg" alt="Lock icon">
      <input 
        class="input"
        value={password}
        on:input={onPasswordChange}
        name="password" 
        type={showPassword ? "text":"password"} 
        placeholder="Enter password">
    </div>
    <button type="button" on:click={toggleVisibility} class="hide-btn {showPassword ? "active" : ""}">
      <img src="./assets/eye.svg" alt="Eye icon">
    </button>
  </div>
</article>

<style>
  * {
    font-family: 'Inter', sans-serif;
    color: #132B50
  }

  .password-form {
    width: 414px;
  }

  .input-label {
    font-size: 14px;
    
    font-weight: 600;
  }

  .input-container {
    margin-top: 8px;
    display: flex;
    align-items: center;
  }

  .password-input {
    flex: 1;
    display: flex;
    padding: 16px;
    border: 1px solid #132B50;
    border-radius: 8px;
  }

  .input-icon {
    width: 27px;
    height: 27px;
    margin-right: 10px;
  }

  .input {
    border: 0;
    font-size: 14px;
    width: 100%;
  }

  .input:focus-visible {
    outline: 0;
  }

  .hide-btn {
    background: none;
    border: 0;
    margin-left: 16px;
    height: 32px;
    width: 32px;
    display: flex;
    justify-content: center;
    align-items: center;
    border-radius: 100%;
    transition: ease-in;
  }

  .hide-btn.active {
    background-color: rgba(19, 43, 80, 0.2);
  }

  .hide-btn:hover {
    background-color: rgba(19, 43, 80, 0.2);
    cursor: pointer;
  }

  .hide-btn:active {
    background-color: rgba(19, 43, 80, 0.5);
  }
</style>