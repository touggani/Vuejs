<template>
  <div>
      <ul>
          <li v-for="l in list" :key="l">{{l}}</li>
      </ul>
  </div>
</template>

<script>
//import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'exo2',
  components: {
  }, 
  data: () => {
    return {
        list: [
            'index0',
            'index1',
            'index2'
        ]
    }
  },
  methods: {
    filters:{
        uppercase(val){
            return val.toUpperCase();
        }
    }
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