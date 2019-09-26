const App = new Vue ({
    el: "#contenedor",
    data: {
        titulo: "Tareas con Vue :)",
        imagen: "",
        tareas: [
            { nombre: "Comprar", estado: true, },
            { nombre: "Estudiar",  estado: false, },
            { nombre: "Comer", estado: false, },
            { nombre: "Pintar", estado: true, },
        ],
    },
    methods: {
        quitarTarea: function(tarea) {
            this.tareas.splice(this.tareas.indexOf(tarea),1);
        },
        addTarea: function(e) {
            event.preventDefault();
            console.log("hola lokaso");
            this.tareas.push({
                nombre: this.tareas.nombre,
                estado: false,
            });
            this.tareas.nombre = '';
        }
    }
})