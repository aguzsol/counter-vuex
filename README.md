# counter-vuex

[imagen del proyecto](https://github.com/aguzsol/counter-vuex/blob/main/Captura%20de%20pantalla%202021-02-11%20a%20las%2012.25.04.png)

Proceso ejercicio:

1. crear componente: CounterComponent.vue
2. importarlo en app.vue
3. pasar bien el html, pensar donde van los estilos(app general o componente). Copiar html container en el componente(template). Copiar estilos generales en la app y estilos del contador en el componente.
4. añadir bootstrap con npm: instalar con el npm en terminal : npm install bootstrap@next. Lo instala en node modules.
5. importar bootstrap en nuestro proyecto: import 'bootstrap/dist/css/bootstrap.min.css' en el main.js
6. añadir funcionalidad counter en el componente: copiar script y interpolaciones al componente.

--- parte 2 ---
7. cuando hacemos click en el otro cambia entre 2 componentes: countercomponent o showcounter
7. crear y construir el componente ShowCounter
8. en app.vue añadir en el export default:
    
   data() {
        return {
        selectedComponent: 'counter-component'
        }
    }

9. en el template app.vue:    `<component:is="selectedComponent"></component>`

10. añadir el evento click en el logo en el tag img. 
11. añadir el metodo changeComponent del click en metodos:
    methods: {
        changeComponent() {
        this.selectedComponent = this.selectedComponent == 'counter-component' ? 'show-counter': 'counter-component'
        }
    },

--- parte 3 --- 
instalar vuex (ya lo hemos hecho al principio al crear el proyecto con "vue create counter-vuex")
12. 


## Project setup
```
npm install
```

### Compiles and hot-reloads for development
```
npm run serve
```

### Compiles and minifies for production
```
npm run build
```

### Lints and fixes files
```
npm run lint
```

### Customize configuration
See [Configuration Reference](https://cli.vuejs.org/config/).
# counter-vuex
