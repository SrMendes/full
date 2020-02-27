<template>
  <v-app>
    <div>
    
    <v-alert
      outlined
      type="success"
      text
    >
      Vuetify Rodando com Sucesso!
       
  {{info.id}}
    </v-alert>
    
  </div>
  <h1>CHORAAAAAAAAA</h1>
        
  </v-app>
</template>

<script>
import HelloWorld from './components/HelloWorld';
import axios from 'axios'
import VueAxios from 'vue-axios'

export default {
  name: 'App',

  components: {
    HelloWorld,
  },

  data: () => ({
    info:{}
  }),
  mounted () { 
    axios.get('http://localhost:3000/users')
      .then(response => (this.info = response.data))
  }
};
</script>
