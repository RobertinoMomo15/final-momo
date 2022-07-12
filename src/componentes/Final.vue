<template>

  <section class="src-componentes-final">
    <div class="jumbotron">
      
      <label>Color:</label>
      <input type="text" v-model="color">
      <hr>
      <label>Fondo:</label>
      <input type="text" v-model="fondo">
      <hr>
      <label>Size:</label>
      <input type="number" v-model="size">
      <hr>

      <label>Texto:</label>
      <input type="text" v-model="texto" :style="getEstilo">


      <segundo v-show="texto " :texto="texto"  />

    </div>

    
      <table class="table table-dark">
        <tr>
          <th>Pregunta</th>
          <th>Respuesta</th>
        </tr>
        
        <tr>
          <td>1</td>
          <td>B</td>
        </tr>
        <tr>
          <td>2</td>
          <td>C</td>
        </tr>
        <tr>
          <td>3</td>
          <td>B</td>
        </tr>
        <tr>
          <td>4</td>
          <td>D</td>
        </tr>
        <tr>
          <td>5</td>
          <td>D</td>
        </tr>


      </table>


  </section>

</template>

<script>
  
  import segundo from './segundo.vue'

  export default  {
    name: 'src-componentes-final',
    components:{
      segundo
    },
    props: [],
    mounted () {

    },
    data () {
      return {
        texto: "",
        color:"",
        fondo:"",
        size: ""
      }
    },
    methods: {

    },
    computed: {
      getEstilo(){
      return { 
        'color': this.color,
        'background-color': this.fondo,
        'font-size': this.size + 'px'
      }
    }
    }
}


</script>

<style scoped lang="css">
  .src-componentes-final {

  }
</style>
