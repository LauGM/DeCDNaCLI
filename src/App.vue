<template>
  <div id="app">
    <tabla-cli :titulo="titulo[0]" :miarray="listaSoporte" :misestilos="estilosSoporte" :miencabezado="encabezado"/>
    <tabla-cli :titulo="titulo[1]" :miarray="listaDirectivos" :misestilos="estilosDirectivos" :miencabezado="encabezado"/>
    <tabla-cli :titulo="titulo[2]" :miarray="listaIt" :misestilos="estilosIt" :miencabezado="encabezado"/>
  </div>
</template>

<script>
import TablaCli from './components/TablaCli.vue'

export default {
  name: 'App',
  components: {
    TablaCli
  },
  data(){
    return{
      titulo:["Usuarios de Soporte Tecnico","Usuarios del Area de Gerencia","Usuarios de Sector It"],
          listaSoporte:[
              {usuario:"@lucc__34",clave:"45Ad45"},
              {usuario:"@starwars10",clave:"St4rW4rs"},
              {usuario:"@Jimenez99",clave:"yo8787*"}
          ],
          listaDirectivos:[
              {usuario:"@TorresJuanManuel",clave:"**9090A"},
              {usuario:"@PerezAlberto",clave:"P*12345"},
              {usuario:"@GonzalezHugo",clave:"yo8787*"}
          ],
          listaIt:[
              {usuario:"@linux2022",clave:"L1nux2022_"},
              {usuario:"@SteveJobs",clave:"mac9876"},
              {usuario:"@ProgrammerX",clave:"101011Binary"}
          ],
          estilosSoporte:"table table-striped",
          estilosDirectivos:"table table-bordered text-danger",
          estilosIt:"table table-dark",
          encabezado:true

    }
          
  }
}
</script>
