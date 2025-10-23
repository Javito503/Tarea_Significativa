<template>
  <div class="investigacion-social">
    <header class="page-header">
      <h1>Investigación y Proyección Social</h1>
      <nav class="breadcrumb">
        <ul>
          <li><router-link to="/">Institución</router-link></li>
          <li>Investigación y Proyección Social</li>
        </ul>
      </nav>
    </header>

    <section class="intro">
      <p>…texto de introducción…</p>
    </section>

    <section class="programas">
      <div class="programa">
        <img src="ruta/a/imagen1.jpg" alt="Programa de Investigación Aplicada">
        <h2>Programa de Investigación Aplicada</h2>
        <p>Texto explicativo …</p>
      </div>
      <div class="programa">
        <img src="ruta/a/imagen2.jpg" alt="Programa de Proyección Social">
        <h2>Programa de Proyección Social</h2>
        <p>Texto explicativo …</p>
      </div>
    </section>

    <footer class="page-footer">
      <p>…pie de página …</p>
    </footer>
  </div>
</template>

<script>
export default {
  name: 'InvestigacionSocial'
}
</script>

<style scoped>
/* Aquí los estilos para que coincida con la página original */
.investigacion-social { /* contenedor principal */ }
.page-header { /* estilos del header, fondo, padding */ }
.breadcrumb ul { list-style: none; display: flex; }
.breadcrumb li + li:before { content: "›"; margin: 0 0.5em; }
/* etc. */
.programas { display: flex; flex-wrap: wrap; gap: 2rem; }
.programa img { width: 100%; max-width: 400px; }
/* agrega colores, tipografías, márgenes para que coincida */
</style>
