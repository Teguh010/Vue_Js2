<template>
  <div>
    <v-container class="my-5">
      <v-card class="auth-tabs">
        <v-toolbar
        >
          <v-tabs
           background-color="transparant"
            v-model="tabs"
            fixed-tabs
          >
            <v-tab name="login">
            Login
            <v-icon right>mdi-account</v-icon>
          </v-tab>

          <v-tab name="register">
            Register
            <v-icon right>mdi-account-plus</v-icon>
          </v-tab>
      
          </v-tabs>
        </v-toolbar>

        <v-tabs-items v-model="tabs">
          <v-tab-item  name="login">
            <login-register :tabs="tabs" />
          </v-tab-item>

          <v-tab-item  name="register" >
          <login-register :tabs="tabs" />
          </v-tab-item>
        </v-tabs-items>
      </v-card>
  </v-container>
  </div>
</template>


<script>
/* eslint-disable */
// import Register from '../components/Auth/LoginRegister.vue'
	export default {
		data () {
	    return {
	      tabs: 'login',
	    }
	  },
	  components: {
	  	'login-register': require('../components/Auth/LoginRegister.vue').default
	  },
	}
</script>

<style>
	.auth-tabs {
		max-width: 500px;
		margin: 0 auto;
	}
</style>