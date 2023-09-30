<template>
  <div id="app">
    <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
    <Jobs/>
  </div>
</template>

<script>

import Jobs from './components/Jobs.vue'

export default {
  name: 'App',
  components: {
    Jobs,
  }
}
// asi es como importo un componente, primero uso el nombre 
// con el que lo exporté en mi componente original, ejemplo Jobs y de ahí
// lo importo, con el nombre from y le pongo el . y todo eso para referirme a la carpeta 
// components para referirme al archivo de Jobs.vue . Finalmente en el export default 
// le digo que use ese componente llamado Jobs, asi mismo si tengo mas componenetes dentro del app.
// Y llamo a Jobs por su nombre, es decir la primera en mayuscula porque todo componente siempre empieza
// en mayuscula. Recuerda que los imports no se separan por comas, se separan por lineas separadas,
//los components sí se se separan por comas
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

</style>
