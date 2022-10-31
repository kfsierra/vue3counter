<template>

    <div class="container">
        <img src="./assets/logo.svg" alt="logo de vue" width="125" height="125">
        <small>
            <h1>Hola gonorreitas desde vue js</h1>
        </small>
        <hr>

        <h2>Contador: {{ contador }}</h2>

        <ShadowButton text="+1" @click="incrementarContador()"/>
        <ShadowButton text="-1" @click="decrementarContador()"/>
        <ShadowButton text="Reset" @click="resetContador()"/>

    </div>
    
</template>

<script>

    import ShadowButton from './buttons/ShadowButton.vue'
    export default {
        components: {
            ShadowButton
        },

        data: () => ({
            contador: 10
        }),

        methods: {

            incrementarContador() {
                this.contador++;
            },

            decrementarContador() {
                this.contador--;
            },

            resetContador() {
                this.contador = 10;
            }

        }

    }

</script>

<style scoped>

    .container {
        text-align: center;
    }
    
    h1 {
        font-weight: bolder;
    }

    small {
        color: #666;
    }

    h2 {
        font-size: 2.5rem;
    }

</style>