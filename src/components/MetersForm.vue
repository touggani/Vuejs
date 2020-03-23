<template>
    <form action="">
        <label for="km">KM : </label>
        <input id="km" type="number" v-model="km"> <br/>
        <label for="m">M : </label>
        <input id="m" name="m" type="number" v-model="m"><br/>
        <label for="cm">CM : </label>
        <input id="cm" type="number" v-model="cm"><br/>
        <label for="mm">MM : </label>
        <input id="mm" type="number" v-model="mm">
    </form>
</template>

<script type="text/javascript">
    export default {
        data() {
            return {
                km: 0,
                m: 0,
                cm: 0,
                mm: 0
            }
        },
        watch: {
            km(val) {
                this.m = val * 1000;
            },
            m(val) {
                this.km = val / 1000;
                this.cm = val * 100;
            },
            cm(val) {
                this.m = val / 100;
                this.mm = val * 10;
            },
            mm(val) {
                this.cm = val / 10;
            }
        }

    }
</script>

<style>
    label {
        display: block;
    }

    input {
        display: block;
    }
</style>


