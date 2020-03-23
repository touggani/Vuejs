<template>
    <div>
        <input v-model="text" placeholder="Entrez liste!" />
        <button v-on:click="ajouter" type="button"> Ajoutez !</button>
        <div v-for="element in liste" v-bind:key="element">
            <span>{{element}}</span>
            <button v-on:click="suprimer(element)" type="button">Supprimez !</button>
        </div>
        
    </div>
</template>

<script>
export default {
    name: 'ToDoList',
    data: function() {
        return {
            text:"",
            liste:[]
        }
    },
    methods:{
        ajouter(){
            this.liste.push(this.text);
            console.log(this.liste);
        },
        suprimer(element){
            const pos = this.liste.indexOf(element);
            this.liste.splice(pos, 1);
        }
    }
}
</script>

<style>

</style>