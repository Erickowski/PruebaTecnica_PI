<template>
  <main class="form-container">
    <h2>Formulario</h2>
    <p>Por favor complete el siguiente formulario.</p>
    <form>
      <input v-model="name" type="text" placeholder="Nombres*" />
      <input v-model="address" type="text" placeholder="Dirección" />
      <select v-model="genre">
        <option value="" disabled selected>Genero</option>
        <option value="F">Femenino</option>
        <option value="M">Masculino</option>
      </select>
      <legend>* Campos requeridos</legend>
      <button v-on:click="putData" type="submit">Enviar</button>
    </form>
  </main>
</template>

<script>
import axios from 'axios'
import Swal from 'sweetalert2'

export default {
  data() {
    return {
      name: '',
      address: '',
      genre: '',
    }
  },
  methods: {
    putData(e) {
      e.preventDefault()
      if (this.name == '') {
        Swal.fire('Llena los campos obligatorios')
      } else {
        axios
          .put('https://jsonplaceholder.typicode.com/users/1', {
            name: this.name,
            address: this.address,
            genre: this.genre,
          })
          .then((res) => {
            if (res.status == 200) {
              Swal.fire(
                '¡Operación con exito!',
                'Los datos han sido actualizados.',
                'success'
              )
            } else {
              Swal.fire(
                '¡Hubo un error!',
                'Ocurrio un problema inesperado.',
                'error'
              )
            }
          })
      }
    },
  },
}
</script>

<style>
.form-container {
  margin: 10px 0 25px;
  padding: 0 50px;
}
form {
  display: flex;
  flex-direction: column;
}
form input,
form select {
  height: 50px;
  margin: 15px 0;
  padding: 10px;
  background-color: #eee;
  outline: none;
  border: none;
  border-radius: 10px;
}
form input::placeholder,
form select {
  color: black;
  font-weight: bold;
  font-size: 18px;
}
form button {
  margin: 25px 0;
  padding: 20px 0;
  text-transform: uppercase;
  font-size: 24px;
  font-weight: bold;
  color: white;
  background: rgb(0, 212, 255);
  background: linear-gradient(
    145deg,
    rgba(0, 212, 255, 1) 0%,
    rgba(9, 9, 121, 1) 100%
  );
  border: none;
  border-radius: 10px;
}
</style>
