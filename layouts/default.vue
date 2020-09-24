<template>
  <div>
    <header>
      <svg
        xmlns="http://www.w3.org/2000/svg"
        height="24"
        viewBox="0 0 24 24"
        width="24"
        v-show="!showMenu"
        v-on:click="toggleShowMenu"
      >
        <path d="M0 0h24v24H0z" fill="none" />
        <path d="M3 18h18v-2H3v2zm0-5h18v-2H3v2zm0-7v2h18V6H3z" />
      </svg>
      <svg
        xmlns="http://www.w3.org/2000/svg"
        height="24"
        viewBox="0 0 24 24"
        width="24"
        v-show="showMenu"
        v-on:click="toggleShowMenu"
      >
        <path d="M0 0h24v24H0z" fill="none" />
        <path
          d="M19 6.41L17.59 5 12 10.59 6.41 5 5 6.41 10.59 12 5 17.59 6.41 19 12 13.41 17.59 19 19 17.59 13.41 12z"
        />
      </svg>
      <h1>{{ title }}</h1>
    </header>
    <nav v-show="showMenu">
      <ul>
        <li><a href="">Captura de datos</a></li>
        <li><a href="">Mi perfil</a></li>
      </ul>
    </nav>
    <Nuxt />
    <footer></footer>
  </div>
</template>

<script>
export default {
  data() {
    return {
      title: 'Home',
      showMenu: false,
    }
  },
  methods: {
    toggleShowMenu() {
      this.showMenu = !this.showMenu
    },
  },
}
</script>

<style>
html {
  font-family: 'Source Sans Pro', -apple-system, BlinkMacSystemFont, 'Segoe UI',
    Roboto, 'Helvetica Neue', Arial, sans-serif;
  font-size: 16px;
  word-spacing: 1px;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
  box-sizing: border-box;
}

*,
*::before,
*::after {
  box-sizing: border-box;
  margin: 0;
}
header {
  position: sticky;
  top: 0;
  z-index: 2;
  width: 100vw;
  padding: 10px;
  display: flex;
  justify-content: flex-start;
  align-items: center;
  -webkit-box-shadow: 0px 5px 10px 0px rgba(0, 0, 0, 0.3);
  -moz-box-shadow: 0px 5px 10px 0px rgba(0, 0, 0, 0.3);
  box-shadow: 0px 5px 10px 0px rgba(0, 0, 0, 0.3);
}
header svg {
  width: 36px;
  height: 36px;
  margin-right: 20px;
  cursor: pointer;
}
header h1 {
  text-transform: uppercase;
}
nav {
  position: absolute;
  top: 100;
  z-index: 1;
  width: 80%;
  height: 100vh;
  padding: 50px 0;
  background-color: white;
  -webkit-box-shadow: 10px 6px 10px 0px rgba(0, 0, 0, 0.3);
  -moz-box-shadow: 10px 6px 10px 0px rgba(0, 0, 0, 0.3);
  box-shadow: 10px 6px 10px 0px rgba(0, 0, 0, 0.3);
}
nav ul {
  list-style: none;
}
nav ul li {
  margin: 20px 0;
}
nav ul li a {
  text-decoration: none;
  color: black;
  font-size: 24px;
  font-weight: bold;
}
footer {
  position: fixed;
  bottom: 0;
  width: 100vw;
  height: 200px;
  background-image: url('../assets/Footer.png');
  background-position: center;
  background-size: cover;
  background-repeat: no-repeat;
}
</style>
