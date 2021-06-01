<template>
  <div id="app">
    <download-excel :data="json_data" :fields="json_fields" worksheet="work_sheet_name" name="excel_name" >
      <button type="button" class="btn btn-success">
        Exportar para o Excel
      </button>
    </download-excel>
  </div>
</template>

<script>
export default {
  name: 'app',
  data(){
    return{ 
      json_fields: {
        "Registro": 'id',
        "Nome": 'name',
        "Sobrenome": 'surname',
        "Idade": 'age',
        "Telefone Residencial": 'phone.home',
        "Telefone Celular": 'phone.work',
        "Data de Registro":{
          field:'birthDate',
        },
      },
      json_data:[
        {
          id:1,
          name:'Demostenes',
          surname:'Brito',
          age:90,
          phone: {
            home: '494933838',
            work: '493780494',
          },
          birthDate:new Date(),
        },
        {
          id:2,
          name:'Demostenes',
          surname:'Brito',
          age:28,
          phone: {
            home: '349493838',
            work: '780493494',
          },
          birthDate:new Date(),
        },
        {
          id:3,
          name:'Demostenes',
          surname:'Brito',
          age:32,
          phone: {
            home: '383832938',
            work: '734949434',
          },
          birthDate:new Date(),
        },
      ]
    }
  }
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
</style>
