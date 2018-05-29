<template>
  <div class="hello">
    <h1>{{ msg }}</h1>

    <componente-simple v-for="item in items" 
      :key="item"
      :mensaje="item"
      @notificar="notificar_papa">
    </componente-simple>

  </div>
</template>

<script>
import ComponenteSimple from '@/components/ComponenteSimple'

export default {
  components: {
    ComponenteSimple
  },
  name: 'HelloWorld',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App',
      items: ["Primero", "Segundo", "Tercero"]
    }
  },
  methods:{
    notificar_papa(hijo){
      this.msg = `${hijo} clickeado`;
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
