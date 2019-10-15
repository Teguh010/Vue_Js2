<template>
  <nav>

    <v-app-bar text app>
      <v-app-bar-nav-icon @click="drawer = !drawer" class="grey--text"></v-app-bar-nav-icon>
      <v-toolbar-title class="text-uppercase grey--text">
        <span class="font-weight-light">Coba</span>
        <span>Table</span>
      </v-toolbar-title>
      <v-spacer></v-spacer>
      <v-btn
        to="/auth" 
        text color="grey">
        <span>Sign In</span>
        <v-icon right>mdi-exit-to-app</v-icon>
      </v-btn>
    </v-app-bar>

    <v-navigation-drawer app v-model="drawer" class="primary">
      <v-layout column align-center>
        <v-flex class="mt-5">
            <v-btn text>
                <img src="/logo-gpsku.png" width="150" style="padding: 5px;">
            </v-btn>
          <!-- <v-avatar size="100">
            <img class="text-lg-center" src="/logo-gpsku.png">
          </v-avatar> -->
          <!-- <p class="white--text subheading mt-1">The Net Ninja</p> -->
        </v-flex>
      </v-layout>
      <!-- <v-list>
        <v-list-tile v-for="link in links" :key="link.text" router :to="link.route">
          <v-list-tile-action>
            <v-icon class="white--text">{{ link.icon }}</v-icon>
          </v-list-tile-action>
          <v-list-tile-content>
            <v-list-tile-title class="white--text">{{ link.text }}</v-list-tile-title>
          </v-list-tile-content>
        </v-list-tile>
      </v-list> -->
      <!-- <v-list  shaped>
      <v-subheader>REPORTS</v-subheader>
      <v-list-item-group v-model="links" color="primary">
        <v-list-item
         v-for="link in links" :key="link.text" router :to="link.route"
        >
          <v-list-item-icon>
            <v-icon v-text="link.icon"></v-icon>
          </v-list-item-icon>
          <v-list-item-content>
            <v-list-item-title v-text="link.text"></v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list-item-group>
    </v-list> -->
    <v-list shaped>
      <v-subheader>REPORTS</v-subheader>
      <v-list-item-group v-model="item" color="white">
        <v-list-item
          v-for="(item, i) in items"
          :key="i"
        >
          <v-list-item-icon>
            <v-icon v-text="item.icon"></v-icon>
          </v-list-item-icon>
          <v-list-item-content>
            <v-list-item-title v-text="item.text"></v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list-item-group>
    </v-list>
    </v-navigation-drawer>

  </nav>
</template>

<script>

  export default {
    data: () => ({
      drawer: true,
      item: 1,
      items: [
        { text: 'Real-Time', icon: 'mdi-clock' },
        { text: 'Audience', icon: 'mdi-account' },
        { text: 'Conversions', icon: 'mdi-flag' },
      ],
    }),
  }
</script>

<style>

</style>
