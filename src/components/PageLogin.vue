<template>
  <div class="container-fluid" id="login-container">
    <section id="section-content">
      <NavBar />
      <main class="container">
        <section class="mx-auto col-sm-5 py-5" id="login-content">
          <h2>Sign in to Coinbase</h2>
          <div class="alert alert-success" v-if="displayAlert" role="alert">
            You have been logged in successfully
          </div>
          <LoginForm @submitted="displayAlert = true"  />
          <div class="d-flex justify-content-between">
            <span v-for="(link, index) in triLinks" :key="index">
              <a :href="link.href">{{link.text}}</a>
            </span>
          </div>
          <a href="https://support.coinbase.com/customer/en/portal/articles/2488794-troubleshooting-2-factor-authentication">Have an issue with 2-factor authentication?</a>
        </section>
      </main>
    </section>
  </div>
</template>

<script>
import NavBar from './NavBar.vue'
import LoginForm from './LoginForm.vue'
export default {
  name: 'Login',
  components: { NavBar, LoginForm },
  data: function(){

    return {
      triLinks: [
        { href: 'https://www.coinbase.com/password_resets/new', text: 'Forgot password?'},
        { href: 'https://www.coinbase.com/signup', text: `Don't have an account?`},
        { href: 'https://www.coinbase.com/legal/privacy', text: 'Privacy Policy'},
      ],
      displayAlert: false,
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

#login-container {
  background-color: #0667d0;
  height: 100vh;
  padding: 0;
  color: white !important;
}

#section-content {
  background-color: inherit;
  height: 535px;
  display: flex;
  flex-direction: column;
}

#section-content > main {
  flex-grow: 2;
  display: flex;
}

#login-content {
   text-align: center; 
   display: flex;
   flex-direction: column;
   justify-content: space-between;  
}

a {
  color: white
}




/*@media only screen and (max-width: 600px) {
  #login-container {
    background-color: #0667d0;
    height: 100vh;
  }
}*/

</style>
