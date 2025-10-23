<template>
  <div class="cursos-diplomados">
    <header class="page-header">
      <h1>Cursos y Diplomados</h1>
      <nav class="breadcrumb">
        <ul>
          <li><router-link to="/">Institución</router-link></li>
          <li>Cursos y Diplomados</li>
        </ul>
      </nav>
    </header>

    <section class="campus-selector">
      <h2>Cursos y Diplomados por campus</h2>
      <p>Selecciona la regional de tu interés y te mostraremos los cursos que ofertamos</p>
      <ul class="campus-list">
        <li><button @click="selectCampus('Santa Tecla')">SANTA TECLA</button></li>
        <li><button @click="selectCampus('Santa Ana')">SANTA ANA</button></li>
        <li><button @click="selectCampus('Zacatecoluca')">ZACATECOLUCA</button></li>
        <li><button @click="selectCampus('San Miguel')">SAN MIGUEL</button></li>
        <li><button @click="selectCampus('La Unión')">LA UNIÓN</button></li>
      </ul>
    </section>

    <section class="about-section">
      <h2>Acerca</h2>
      <p>En La Escuela Especializada en Ingeniería ITCA-FEPADE estamos comprometidos con la calidad académica, la empresarialidad y la pertinencia de nuestra oferta educativa.</p>
    </section>

    <section class="course-categories">
      <h2>Cursos</h2>
      <ul>
        <li>Academia CISCO</li>
        <li>Gastronomía</li>
        <li>Mecatrónica, Electrónica e Industria 4.0</li>
        <li>Idiomas</li>
        <li>Tecnologías Informáticas</li>
        <li>Eléctrica, Automotriz, Mecánica Industrial, Civil y Construcción</li>
      </ul>
    </section>

    <!-- Aquí podrías añadir el listado concreto de cursos según campus seleccionado -->

    <footer class="page-footer">
      <p>© Escuela Especializada en Ingeniería ITCA-FEPADE. Todos los derechos reservados.</p>
      <address>Carretera a Santa Tecla km. 11, La Libertad, El Salvador C.A. Tel. (503) 2132-7400</address>
    </footer>
  </div>
</template>

<script>
export default {
  name: 'CursosDiplomados',
  data() {
    return {
      selectedCampus: null,
      // podrías tener un objeto con los cursos por campus para mostrar
    }
  },
  methods: {
    selectCampus(campus) {
      this.selectedCampus = campus;
      // lógica para mostrar los cursos correspondientes
    }
  }
}
</script>

<style scoped>
.cursos-diplomados {
  padding: 2rem;
  font-family: /* poner la fuente usada por ITCA-FEPADE */;
}
.page-header {
  background-color: #f5f5f5; /* o el color que use la página */
  padding: 2rem 0;
  text-align: center;
}
.breadcrumb ul {
  list-style: none;
  display: flex;
  justify-content: center;
  gap: 0.5rem;
  padding: 0;
}
.breadcrumb li + li:before {
  content: "›";
  margin: 0 0.5rem;
}
.campus-selector {
  text-align: center;
  margin: 3rem 0;
}
.campus-list {
  display: flex;
  flex-wrap: wrap;
  gap: 1rem;
  justify-center: center;
}
.campus-list button {
  padding: 1rem 2rem;
  border: none;
  background-color: #007bff; /* azul ejemplo */
  color: white;
  cursor: pointer;
  border-radius: 4px;
}
.campus-list button:hover {
  background-color: #0056b3;
}
.about-section {
  margin: 3rem 0;
}
.course-categories ul {
  list-style: disc;
  margin: 1rem 0 2rem 2rem;
}
.page-footer {
  text-align: center;
  margin: 4rem 0 0;
  font-size: 0.9rem;
  color: #666;
}
.page-footer address {
  font-style: normal;
}
@media (max-width: 768px) {
  .campus-list {
    flex-direction: column;
    align-items: center;
  }
}
</style>
