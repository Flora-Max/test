<template>
  <div id="app">
    <Home/>
  </div>
</template>


<script>
import TheHeader from './components/TheHeader.vue';
import { ref } from 'vue';
import Home from './pages/home.vue'

export default {
  name: 'App',
  components: {
    Home
  }
}

</script>


<style scoped>
  #app{
    padding: 20px;
  }
</style>

