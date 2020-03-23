<template>
  <div id="app">
    <div class="carousel">
     <img v-bind:src="list[imageIndex]">
    </div>
    <button v-on:click="getPreviewImage()">Precedent</button>
    <button v-on:click="getNextImage()">Suivant</button>
    
  </div>
</template>

<script>
import logo from '../assets/logo.png';

export default {
  name: 'App',
  components: {
  }, 
  data: () => {
    return {
      list: [
        logo,
        logo,
        logo
        ], 
        imageIndex: 0
    }
  },
  methods: {
    getNextImage(){
        if(this.imageIndex > this.list.length-1){
            alert(this.list.length);
            this.imageIndex = 0;
        }
        else{
            this.imageIndex ++;
        }
    },
    getPreviewImage(){
        if(this.imageIndex < 0){
            this.imageIndex = this.list.length;
        }
        else{
            this.imageIndex --;
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
