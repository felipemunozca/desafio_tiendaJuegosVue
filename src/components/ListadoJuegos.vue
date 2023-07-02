<template>
    <div class="container mt-5">
        <div class="bg-info-subtle py-2 px-4">
            <h2>¡Bienvenido!</h2>
            <hr>
            <p>A continuación encontraras una lista de los juegos que prefieres</p>
        </div>
        <div class="m-auto col-8 mt-5">
            <table class="table table-dark table-bordered border-white text-center">
                <thead>
                    <tr>
                        <th scope="col">#</th>
                        <th scope="col">Juego</th>
                        <th scope="col">Eliminar Juego de la lista</th>
                    </tr>
                </thead>
                <tbody>
                    <tr v-for="(juego, index) in games" :key="index">
                        <th scope="row">{{index}}</th>
                        <td>{{juego}}</td>
                        <td><button @click="eliminarJuegoHijo(index)" class="btn btn-danger">Eliminar</button></td>
                    </tr>
                </tbody>
            </table>
        </div>
    </div>
</template>

<script>
export default {
    name: 'juegos-comp',
    props: {
        games: {
            type: Array,
            required: true,
        }
    },
    data: function(){
        return {}
    },
    // computed: {},
    methods: {
        eliminarJuegoHijo(index) {
            this.$emit('eliminarJuego', index)
        }
    }
    // watch: {},
    // components: {},
    // mixins: [],
    // filters: {},
    // -- Lifecycle Methods
    // -- End Lifecycle Methods
}
</script>

<style scoped>
    
</style>