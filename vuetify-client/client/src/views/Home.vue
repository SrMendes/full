<template>
  <div>
   
    <v-alert
      outlined
      type="success"
      text
    >
      Você está na Home!
    </v-alert>
    
  </div>
  
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'

export default {
  name: 'Home',
  components: {
    HelloWorld
  }
}
</script>
