<template>
 <v-form @submit.prevent="submitForm">
     <v-container>
      <v-row>

        <v-col cols="12" sm="12" md="12">
        <v-banner class="grey col">
            <v-icon
            slot="icon"
            color="primary"
            size="36"
            >
            mdi-account-circle
            </v-icon>
           
            Silahkan Mendaftar untuk bisa masuk
        </v-banner>
       </v-col>
          <!-- <v-col cols="12" sm="6"> -->
           <v-col cols="12" sm="12" md="12">
            <v-text-field
            v-model="formData.email"
            :rules="[ val => validateEmail(val) || 'Silahkan masukan Email yang valid']"
              ref="email"
              outlined
              label="Email"
              append-outer-icon="mdi-shield-account"
            ></v-text-field>
            <v-text-field
            v-model="formData.password"
            :rules="[ val => val.length >= 6 || 'Silahkan masukan minimal 6 karakter']"
            ref="password"
              lazy-rules
              outlined
              type="password"
              label="Password"
              append-outer-icon="mdi-shield-account"
            ></v-text-field>
            <div class="text-right">
             <v-btn 
             color="primary"
             type="submit"
            >Register</v-btn>
            </div>
        
            </v-col>
        </v-row>
      </v-container>
    </v-form>
</template>

<script>
/* eslint-disable */
export default {
    props: ['tabs'],
    data() {
        return {
            formData: {
                email: '',
                password: ''
            }
        }
    },
    methods: {
        validateEmail(email) {
             var re = /^(([^<>()\[\]\\.,;:\s@"]+(\.[^<>()\[\]\\.,;:\s@"]+)*)|(".+"))@((\[[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\])|(([a-zA-Z\-0-9]+\.)+[a-zA-Z]{2,}))$/
             return re.test(String(email).toLowerCase())
        },
        submitForm() {
				this.$refs.email.validate()
				this.$refs.password.validate()
				if (!this.$refs.email.hasError && !this.$refs.password.hasError) {
					console.log(this.tabs)
				}
			}
    }
    
}
</script>


<style  scoped>
  /* .bg-grey col {
		display: flex;
		justify-content: center;
	} */

</style>


