<template>
<header class="container">
  <b-navbar class="main-nav" toggleable="md">
    <b-navbar-brand href="https://www.coinbase.com/" id="brand-name">coinbase</b-navbar-brand>

    <b-navbar-toggle target="nav_collapse"></b-navbar-toggle>

    <b-collapse is-nav id="nav_collapse">
      <b-navbar-nav id="nav-links" class="ml-auto">
        <b-nav-item-dropdown id="products-link" text="Products" right>
          <b-dropdown-item href="#">Buy/Sell Digital Currency</b-dropdown-item>
          <b-dropdown-item href="#">Coinbase Pro</b-dropdown-item>
          <b-dropdown-item href="https://prime.coinbase.com">Coinbase Prime</b-dropdown-item>
          <b-dropdown-item href="#">Developer Platform</b-dropdown-item>
          <b-dropdown-item href="#">Coinbase Commerce</b-dropdown-item>
        </b-nav-item-dropdown>

        <b-nav-item href="https://www.coinbase.com/help">Help</b-nav-item>
        <b-nav-item href="https://www.coinbase.com/charts">Charts</b-nav-item>
        <b-nav-item href="https://www.coinbase.com/signin">Sign In</b-nav-item>
        <b-nav-item id="signup-link" href="https://www.coinbase.com/signup">Sign Up</b-nav-item>
      </b-navbar-nav>

    </b-collapse>
  </b-navbar>  
</header>
</template>

<script>
  export default {
    name: 'NavBar'
  }
</script>


<style scoped>
  .main-nav {
    color: white;
  }

  .main-nav a, .main-nav a > * {
    color: white !important;
    font-weight: 600;
    text-decoration: none;
  }



  #brand-name {
    font-weight: bold;
    font-size: 32px;
  }
</style>

<style>
  #products-link > *{
    color: white !important;
    font-weight: bold;
  }

  #products-link .dropdown-item {
    color: #333333 !important;
    font-size: 13px;
  }

  #products-link .dropdown-item:hover {
    color: #2b71b1 !important;
    border: none;
  }

  #signup-link {
    border: 1px solid white;
  }

  #nav-links > * {
    margin: 0 .7rem;
  }
  
</style>



