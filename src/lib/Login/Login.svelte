<svelte:head>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@500;600;700&display=swap" rel="stylesheet">
</svelte:head>

<script>
  import Account from './Account.svelte';
  import ActionBar from './ActionBar.svelte';
  import PasswordInput from './Password-Input.svelte';

  const accountInfo = {
    type: 'Business Account',
    name: 'Sarah Bills'
  };

  let password = "";
</script>

<div style="display: inline-block;">
  <section class="container">
    <h3 class="title">Enter your password</h3>

    <Account account={accountInfo}/>
    <PasswordInput bind:password={password}/>
    <ActionBar disableContinue={password == ""}/>

    <span>
      <a class="reset-password" href="https://google.com/">Reset password</a>
    </span>
  </section>
</div>


<style>
  * {
    font-family: 'Inter', sans-serif;
    color: #132B50
  }

  .container {
    display: grid;
    row-gap: 32px;
    border-radius: 16px;
    padding: 85px;
    box-shadow: 0px 44px 104px 0px rgba(19, 43, 80, 0.1);
    background-color: white;
  }

  .title {
    font-size: 32px;
  }

  .reset-password {
    display: inline;
    font-weight: 600;
    text-decoration: none;
    border-bottom: 1px solid #132B50;
  }
</style>