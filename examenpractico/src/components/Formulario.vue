<template>
    <div class="form-container">
        <h2>Registro de Usuario</h2>
        <form @submit.prevent="submitForm">
            <div class="form-group">
                <label>Nombre:</label>
                <input v-model="nombre" type="text" placeholder="Ingresa tu nombre" />
            </div>

            <div class="form-group">
                <label>Correo:</label>
                <input v-model="correo" type="email" placeholder="ejemplo@gmail.com" />
            </div>

            <div class="form-group">
                <label>Teléfono:</label>
                <input v-model="telefono" type="tel" placeholder="11223344" />
            </div>

            <div class="form-group">
                <label>Dirección:</label>
                <input v-model="direccion" type="text" placeholder="Av. Principal 123" />
            </div>

            <div class="form-group">
                <label>Edad:</label>
                <input v-model="edad" type="number" min="1" max="120" placeholder="Edad" />
            </div>

            <button type="submit">Enviar</button>
        </form>
    </div>
</template>

<script>
export default {
    name: 'Formulario',
    data() {
        return {
            nombre: '',
            correo: '',
            telefono: '',
            direccion: '',
            edad: ''
        }
    },
    methods: {
        submitForm() {
            alert(`Nombre: ${this.nombre}
Correo: ${this.correo}
Teléfono: ${this.telefono}
Dirección: ${this.direccion}
Edad: ${this.edad}`)
        }
    }
}
</script>

<style scoped>
.form-container {
    max-width: 400px;
    margin: 40px auto;
    padding: 20px;
    background-color: #f0f4f8;
    border-radius: 10px;
    box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
}

h2 {
    text-align: center;
    margin-bottom: 20px;
    color: #333;
}

.form-group {
    margin-bottom: 15px;
}

label {
    display: block;
    font-weight: bold;
    margin-bottom: 5px;
    color: #555;
}

input {
    width: 100%;
    padding: 8px 10px;
    border-radius: 5px;
    border: 1px solid #ccc;
    box-sizing: border-box;
}

input:focus {
    outline: none;
    border-color: #007BFF;
}

button {
    width: 100%;
    padding: 10px;
    background-color: #007BFF;
    border: none;
    color: white;
    font-weight: bold;
    border-radius: 5px;
    cursor: pointer;
    transition: background-color 0.3s;
}

button:hover {
    background-color: #0056b3;
}
</style>
