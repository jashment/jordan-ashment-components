<template>
  <v-app>

    <v-toolbar>
      
    
      <v-toolbar-title v-text="title"></v-toolbar-title>
      <v-spacer></v-spacer>
      
    </v-toolbar>
      <ja-header/>
    <v-content v-for="i in 6" style="border-top: 1px solid grey;">
      <h2 style="padding: .25em;"><v-icon style="color: blue; font-size: 1em; padding: 0 .5em;">compare_arrows</v-icon>Server {{ i }}</h2>
      <ja-serverStatus/>
    </v-content>
    <ja-serverDetails/>
    <ja-footer/>
    
  </v-app>
</template>

<script>
import Header from './components/Header.vue'
import ServerDetails from './components/ServerDetails.vue'
import CustomComp from './components/CustomComp.vue'
import ServerStatus from './components/ServerStatus.vue'
import Footer from './components/Footer.vue'


export default {
  name: 'App',
  components: {
    'ja-header': Header,
    'ja-serverDetails': ServerDetails,
    'ja-customComp': CustomComp,
    'ja-serverStatus': ServerStatus,
    'ja-footer': Footer
  },
  data () {
    return {
      clipped: false,
      drawer: true,
      fixed: false,
      items: [{
        icon: 'bubble_chart',
        title: 'Inspire'
      }],
      miniVariant: false,
      right: true,
      rightDrawer: false,
      title: 'Server Status'
    }
  }
}
</script>

