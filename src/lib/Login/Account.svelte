<svelte:head>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@500;600;700&display=swap" rel="stylesheet">
</svelte:head>

<script>
  export let account = {
    type: "Personal Account",
    name: "Sean Rodriguez"
  };
</script>

<article class="account">
  <img class="account-profile" src="https://picsum.photos/78" alt="">
  <div class="account-details">
    <h5 class="account-type">{account.type}</h5>
    <h4 class="account-holder">{account.name}</h4>
  </div>
</article>

<style>
  * {
    font-family: 'Inter', sans-serif;
    color: #132B50;
  }

  .account {
    display: flex;
    align-items: center;
  }

  .account-profile {
    border-radius: 100%;
  }

  .account-details {
    margin-left: 16px;
  }

  .account-type {
    font-size: 14px;
    font-weight: 500;
    margin-bottom: 4px;
  }

  .account-holder {
    font-size: 18px;
  }
</style>