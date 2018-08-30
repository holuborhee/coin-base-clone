<template>
  <b-form @submit="onSubmit" class="card" id="login-form">

    <b-form-input v-model="email"
      type="email"
      required
      placeholder="Email"
      size="sm"
    ></b-form-input>
    <b-form-input v-model="password"
      type="password"
      required
      placeholder="Password"
      size="sm"
    ></b-form-input>
    <div class="d-flex align-items-center justify-content-between">
      <b-form-checkbox 
         v-model="remainSignedIn"
         :value="true"
         :unchecked-value="false"
      >
        Keep me signed in on this computer
      </b-form-checkbox>

      <b-button type="submit" id="btn-submit">SIGN IN</b-button>


    </div>
  </b-form>

</template>


<script>
  export default {
    name: 'LoginForm',
    data(){
      return {
        email: null,
        password: null,
        remainSignedIn: false
      }
    },
    methods: {
      onSubmit: function(){
        this.$emit('submitted')
      }
    }
  }


</script>


<style>
  #login-form {
    height: 220px;
    padding: 2rem 1rem;
    color: #484c57;
    -webkit-box-shadow: 0 1px 46px -4px rgba(0,0,0,.28);
      box-shadow: 0 1px 46px -4px rgba(0,0,0,.28);
  }

  #login-form > * {
    margin: .5rem 0;
  }

  #btn-submit {
    background-image: linear-gradient(#1d90cb,#0e86c4);
    border-color: #137dba;
    font-size: 11px ;
    height: 42px;
  }

</style>