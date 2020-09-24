<template>
  <div>
    <header>
      <svg
        xmlns="http://www.w3.org/2000/svg"
        height="24"
        viewBox="0 0 24 24"
        width="24"
      >
        <path d="M0 0h24v24H0z" fill="none" />
        <path d="M3 18h18v-2H3v2zm0-5h18v-2H3v2zm0-7v2h18V6H3z" />
      </svg>
      <h1>Captura de datos</h1>
    </header>
    <Nuxt />
    <footer></footer>
  </div>
</template>

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
}
header h1 {
  text-transform: uppercase;
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
