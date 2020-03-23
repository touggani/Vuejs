<template>
  <div id="app">
    <!--<exo2 :exo2="exo2"/>-->
    <!--<calculatrice :calculatrice="calculatrice"/>-->
    <!--<MetersForm :MetersForm="MetersForm"/>-->
    <Carouel/>
  </div>
</template>

<script>
//import exo2 from './components/exo2.vue'
//import calculatrice from './components/calculatrice.vue'
//import MetersForm from './components/MetersForm.vue'
import Carouel from './components/Carouel.vue'

export default {
  name: 'App',
  components: {
    //exo2,
    //calculatrice,
    //MetersForm
    Carouel
  }, 
  data: () => {
    return {
      
    }
  },
  methods: {
    
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
