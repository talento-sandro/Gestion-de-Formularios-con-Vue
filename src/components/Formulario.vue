<template>
    <div class="container">
        <form action="">
            <div class="row">
                <div class="col-xs-12 col-sm-8 col-md-6">
                    <h1>Formulario de Contacto</h1>
                    <hr>
                    <div class="form-group">
                        <label for="nombre">Nombre:</label>
                        <input type="text" id="nombre" class="form-control" v-model="datosPersona.nombre">
                    </div>
                    <div class="form-group">
                        <label for="email">E-mail:</label>
                        <input type="text" id="email" class="form-control" v-model="datosPersona.email">
                    </div>
                </div>
            </div>
            <div class="row">
                <div class="col-xs-12 col-sm-8 col-md-6">
                    <label for="mensaje">Mensaje</label> <br>
                    <textarea id="mensaje" cols="60" rows="5" v-model="mensaje"></textarea>
                </div>
            </div>
        </form>

        <div class="row">
            <div class="col-xs-12 col-sm-8 col-md-6">
                <div class="panel panel-default">
                    <div class="panel-heading">
                        <h3>Datos Ingresados</h3>
                    </div>
                    <div class="panel-body">
                        <p>Nombre: {{ datosPersona.nombre }}</p>
                        <p>Email: {{ datosPersona.email}}</p>
                        <p style="white-space: pre">Mensaje: <br> {{mensaje}}</p>   <!-- style="white-space: pre ES NECESARIO PARA QUE SE RESPETEN LOS ENTER una nueva línea al escribir" -->
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
  name: 'formulario',
  data(){
      return{
          datosPersona: {                             // se agrupan en un objeto para un mejor orden
            nombre:'',
            email:''
          },
          mensaje: ''
      }
  }
}
</script>

<style>

</style>
