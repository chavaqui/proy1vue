<template>
 <div class="mostrar">
    <h2>Estamos dentro del componente MostrarExcel. yes!</h2>
    <h3>{{msg}}</h3>
 </div>
</template>

<script>
import axios from "axios";
export default {
  name: 'MostrarExcel',
  props: {
    msg: String
  },
  data: function(){
    return{
      usuario:'',
      //password:'',
      //error: false,
      error_msg:'',
    }
  },
  methods:{

    
    login(){
      axios
        .get("http://127.0.0.1:8000/api_datos_simples/docentes/")
        .then((response) => {
          let user = response.data;

          console.log(user.find(({nombre}) => nombre === this.usuario));
          //console.log(Object.values(user));
          //console.log(user.nombre);
          //Object.values(Object.values(user)).forEach((nombre,staff,admin) => {
          //  console.log('nombre: '+ nombre + ' staff: '+staff+' admin: '+admin);            
          //});
          if ((user.find(({nombre}) => nombre === this.usuario)) !== undefined){
            setTimeout(()=>{
              const target = document.getElementById("alertDiv");
            target.style.visibility = 'hidden';
            },1000);
            console.log('acceso permitido');
            this.error_msg= false
            window.alert("awdawd")
          }else{
            this.error_msg= true
            console.log('acceso denegado');
          }
        });
    }
  }
}
</script>

<style scoped>
h3 {
  margin: 40px 0 0;
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
