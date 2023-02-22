<template>
  <div class="container">
      
      <router-link to="/Crear" class="btn btn-success">Agregar nuevo registro</router-link>
      <br/><br/>
      <div class="card">
        <div class="card-header">
            Días Habiles
        </div>
        <div class="card-header">
            <table class="table">
              <thead>
                <tr>
                  <th>ID</th>
                  <th>TITULO</th>
                  <th>COMPLETADO</th>
                  <th>ACCIONES</th>
                </tr>
              </thead>
              <tbody>
                <tr v-for="dataApi in dataApiC" :key="dataApi.id">
                  <td>{{ dataApi.userId }}</td>
                  <td>{{ dataApi.title }}</td>
                  <td>{{ dataApi.completed }}</td>
                  <td>
                  
                    <div class="btn-group" role="group" aria-label="">
                      <button type="button" class="btn btn-info">Editar</button>
                      <button type="button" class="btn btn-danger">Borrar</button>
                    </div>
                  </td>
                </tr>
              </tbody>
            </table>
        </div>
      </div>
  </div>
</template>
<script>
export default {
data(){
        return {
          dataApiC:[] 
      }
    },

  created:function ()
  {
    this.consultarApi();
  },
  methods:{

    consultarApi(){
      fetch('https://jsonplaceholder.typicode.com/todos/')
      
      .then(respuesta=>respuesta.json())
      .then((datosRespuesta)=>{
        console.log(datosRespuesta)
        this.dataApiC=[]
        
          this.dataApiC=datosRespuesta;
        
      })
      .catch(console.log)
    }
  }
  
}
</script>