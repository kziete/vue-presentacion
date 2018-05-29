<template>
    <div>
        <h2>{{mensaje}}</h2>
        <button @click="notificar">Notificar</button>
    </div>
</template>
<script>
export default {
  props: ["mensaje"],
  data(){
      return {}
  },
  methods: {
      notificar(){
          this.$emit("notificar",this.mensaje);
      }
  }
}
</script>

