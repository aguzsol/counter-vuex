<template>
  <img @click="changeComponent" alt="Vue logo" src="./assets/logo.png">
   <!-- Usando dynamic components y el atributo :is; haz que cada vez que hagamos click en el logo, se cambie el componente que se muestre-->
   <component :is="selectedComponent" />

   <!-- comentar para la parte 2: -->
   <!-- <counter-component></counter-component> --> 
</template>

<script>
import CounterComponent from './components/CounterComponent.vue'

export default {
  name: 'App',

   data() {
    return {
      // al cargar el component por primera vez, seleccionar el CounterComponent
      selectedComponent: 'counter-component'
    }
  },

  methods: {
    changeComponent() {
      this.selectedComponent = this.selectedComponent == 'counter-component' ? 'show-counter': 'counter-component'
    }
  },

  components: {
    CounterComponent
  },

 
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

:root {
  --mainWhite: #f5f5f5;
  --mainGreen: #7fb800;
  --mainBlue: #0d2c54;
  --lightBlue: #00a6ed;
  --mainBlack: #333333;
}
.max-height {
  min-height: 50vh;
}
body {
  /**   background: url("~@/assets/mainBcg.jpeg") center/cover fixed no-repeat; Forma alternativa de añadir los 'assets' en caso de que no fuera bien el uso de la URL relativa
 */
  background: url("~@/assets/blue-gradient-bg-update.jpg") center/cover fixed no-repeat ;
  background-color: var(--mainBlue);
  color: white;
}
.main-container {
  border: 0.1rem solid var(--mainWhite);
  box-shadow: 0 0.5rem 0.5rem rgba(0, 0, 0, 0.9);
  border-radius: 0.2rem;
}
</style>
