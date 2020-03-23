<template>
  <div>
    <input v-model="val1" placeholder="valeur 1">
    <select v-model="selected">
      <option v-for="option in options" :key="option.text" v-bind:value="option.value">
        {{ option.text }}
      </option>
    </select>
    <input v-model="val2" placeholder="valeur 2">
    <button v-on:click="calcul(selected)">resultat</button>
    <p>Le message est : {{ resultat }}</p>
    
  </div>
</template>

<script>
//import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'calculatrice',
  components: {
  }, 
  data: () => {
    return {
      val1 : 0,
      val2 : 0,
      resultat : 0,
      options: [
      { text: 'addition', value: '+' },
      { text: 'soustraction', value: '-' },
      { text: 'multiplication', value: '*' }
      ]
    }
  },
  methods: {
    calcul: function(selected) {
      if(selected == "*"){
        this.resultat = parseInt(this.val1) * parseInt(this.val2);
      }
      if(selected == "+"){
        this.resultat = parseInt(this.val1) + parseInt(this.val2);
      }
      if(selected == "-"){
        this.resultat = parseInt(this.val1) - parseInt(this.val2);
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
