<template>
  <v-container fluid>
    <v-slide-y-transition mode="out-in">
      <v-layout column max-width>

        <v-layout justify-center>

        <img src="/logo-gpsku.png" width="170" style="padding: 5px;" alt="Vuetify.js" class="mb-5">
       
        </v-layout>
        <!-- <div v-for="(contact,index) in contacts" :key='index'>

            <h3>{{contact.mobile}}</h3>
          
        </div> -->
  
    <data-table></data-table>

      </v-layout>
    </v-slide-y-transition>
  </v-container>
</template>

<script>  

import dataTable from './dataTable'

export default {

    // data(){
    //   return {
    //    contacts:[]
    //   }
    // },
    components:{
      dataTable
    }
    // methods:{
    //   fetchContacts(){
    //          axios.get('/contact')
    //       .then(response=>{
    //           console.log(response);
    //           this.contacts=response.data.data;
    //       })
    //   }
    // },
    // mounted(){
    //   this.fetchContacts();
    // },

    // created(){
    // }

}

</script>

<style  scoped>
  /* .mb-5 {
		display: flex;
		justify-content: center;
	} */

</style>