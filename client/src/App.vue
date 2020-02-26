<template>
  <div id="app"> 
    <h1>{{ msg }}</h1>
    
  <div>{{info[0].id}}</div>
  <div>{{info[0].name}}</div>
  <div>{{info[0].email}}</div>
 </div>
    
</template>

<script>
import axios from 'axios'
import VueAxios from 'vue-axios'
import Vue from 'vue'
import App from './App.vue'
Vue.use(VueAxios, axios)

export default {
  name: 'app',
  data () {
    return {
      msg: 'Lista de dados no banco de dados:',
      info: {}
    }
  },
  mounted () { 
    axios.get('http://localhost:3000/users')
      .then(response => (this.info = response.data))
  }
}

</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

h1, h2 {
  font-weight: normal;
}

ul {
  list-style-type: none;
  padding: 0;
}

li {
  display: inline-block;
  margin: 0 10px;
}

a {
  color: #42b983;
}
</style>
