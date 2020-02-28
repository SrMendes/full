<template>
<v-app>
  <router-view></router-view>
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
