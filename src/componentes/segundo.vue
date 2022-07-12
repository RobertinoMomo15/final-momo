<template>

  <section class="src-componentes-segundo">
    <h1>Cantidad de palabras: {{getPalabras}}</h1>
  </section>

</template>

<script>

  export default  {
    name: 'src-componentes-segundo',
    props: ['texto'],
    mounted () {

    },
    data () {
      return {

      }
    },
    methods: {

    },
    computed: {
      getPalabras(){
        var array = this.texto.trim().split(' ')
        var cant = array.length
        
        return cant 
      }
    }
}


</script>

<style scoped lang="css">
  .src-componentes-segundo {

  }
</style>
