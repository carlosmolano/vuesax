<template lang="html">
  <div class="con-select-example">
    <vs-select
      vs-autocomplete
      class="selectExample"
      label="Peliculas"
      v-model="select1"
      :options="options1"
      ></vs-select>
    <vs-select
    vs-autocomplete
    class="selectExample"
      label="Figuras"
      v-model="select3"
      :options="options3"
      ></vs-select>
      <vs-select
      vs-autocomplete
      class="selectExample"
        disabled="true"
        label="Colores"
        v-model="select2"
        :options="options2"
        ></vs-select>
  </div>
</template>

<script>
export default {
  name:'',
  data(){
    return {
      select1:1,
      select2:0,
      select3:0,
      options1:[
        {text:'IT',value:1},
        {text:'Blade Runner',value:2},
        {text:'Thor Ragnarok',value:3},
      ],
      options2:[
        {text:'Rojo',value:0},
        {text:'Verde',value:2},
        {text:'Azul',value:3},
      ],
      options3:[
        {text:'Cuadrado',value:0},
        {text:'Rectángulo',value:2},
        {text:'Rombo',value:3},
        {text:'Romboide',value:4},
        {text:'Trapecio',value:5},
        {text:'Triángulo',value:6},
        {text:'Polígono',value:7},
        {text:'Polígono regular',value:8},
        {text:'Circunferencia',value:9},
        {text:'Círculo',value:10},
        {text:'Sector circular',value:11},
        {text:'Trapecio circular',value:12},
      ]
    }
  },
  methods:{
    prueba(){
      console.log("prueba de focsu");
    }
  }
}
</script>

<style lang="css">
.selectExample {
  margin: 10px;
}
.con-select-example {
  display: flex;
  align-items: center;
  justify-content: center;
}
.con-select .vs-select {
  width: 100%
}
@media (max-width: 550px) {
  .con-select {
    flex-direction: column;
  }
  .con-select .vs-select {
    width: 100%
  }
}
</style>
