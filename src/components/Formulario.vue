<template>
  <div class="container py-5">
    <div class="row">
      <div class="col-xs-12 col-md-6">
        <form action="">
          <h1>Formulario de contacto</h1>
          <hr />
          <div class="form-group">
            <label for="nombre">Nombre</label>
            <input
              type="text"
              name="nombre"
              id="nombre"
              class="form-control"
              v-model="datosPersona.nombre"
            >
          </div>
          <div class="form-group">
            <label for="email">Email</label>
            <input
              type="email"
              name="email"
              id="email"
              class="form-control"
              v-model="datosPersona.email"
            >
          </div>
          <div class="form-group">
            <label for="mensaje">Mensaje</label>
            <textarea
              name="mensaje"
              id="mensaje"
              class="form-control"
              cols="30"
              rows="5"
              v-model="mensaje"
            ></textarea>
          </div>
          <div class="form-check mb-5">
            <input
              class="form-check-input"
              type="checkbox"
              id="enviarmail"
            >
            <label class="form-check-label" for="enviarmail">Enviar Email</label>
          </div>
        </form>
      </div>
      <div class="col-xs-12 col-md-6">
        <div class="card">
          <div class="card-header">
              <h3>Datos ingresados</h3>
          </div>
          <div class="card-body">
            <p>Nombre: {{ datosPersona.nombre}}</p>
            <p>Email: {{ datosPersona.email}}</p>
            <p style="white-space: pre;">Mensaje: {{ mensaje }}</p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>

export default {
  name: 'formulario',
  data() {
    return {
        datosPersona: {
            nombre: '',
            email: ''
        },
        mensaje: 'Test mensaje'
    }
  }
}
</script>

<style>
</style>