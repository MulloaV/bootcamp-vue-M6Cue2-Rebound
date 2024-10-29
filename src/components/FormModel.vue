<template>
    <div>
        <form @submit.prevent="saludo">
            <label for="nombre">Nombre:</label><br>
            <input type="text" id="nombre" v-model="nombre"><br>
            <label for="apellido">Apellido:</label><br>
            <input type="text" id="apellido" v-model="apellido"><br>
            <label for="correo">Correo:</label><br>
            <input type="email" id="correo" v-model="correo"><br>
            <label for="edad">Edad:</label><br>
            <input type="number" id="edad" v-model="edad"><br><br>
            <button type="submit">Enviar</button>
        </form>
        <p v-if="mostrarSaludo">Hola {{ nombre }} {{ apellido }}, tu correo es {{ correo }} y tienes {{ edad }} años</p>
        <br>
        <p v-if="mostrarSaludo">
           Ahora  {{ nombre }} {{ apellido }}, tienes {{ edad }} años, y corresponde a la siguiente etapa: 
            <span v-if="edad >= 0 && edad <= 13">Niñez</span>
            <span v-else-if="edad >= 14 && edad <= 17">Adolescencia.</span>
            <span v-else-if="edad >= 18 && edad <= 35">Adulto joven.</span>
            <span v-else-if="edad >= 36 && edad <= 64">Adulto.</span>
            <span v-else-if="edad >= 65">Tercera edad.</span>
        </p>
    </div>
</template>

<script>
import Vue from 'vue';

export default Vue.extend({
    name: 'FormModel',
    data() {
        return {
            nombre: '',
            apellido: '',
            correo: '',
            edad: '',
            mostrarSaludo: false
        };
    },
    methods: {
        saludo() {
            this.mostrarSaludo = true;
        }
    }
});

</script>


<style lang="scss" scoped>
    
</style>