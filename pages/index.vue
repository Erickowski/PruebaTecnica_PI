<template>
  <main>
    <h2>Formulario</h2>
    <p>Por favor complete el siguiente formulario.</p>
    <form>
      <input type="text" placeholder="Nombres*" />
      <input type="text" placeholder="Dirección" />
      <select>
        <option value="" disabled selected>Genero</option>
        <option value="F">Femenino</option>
        <option value="M">Masculino</option>
      </select>
      <legend>* Campos requeridos</legend>
      <button type="submit">Enviar</button>
    </form>
  </main>
</template>

<script>
export default {}
</script>

<style>
main {
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
