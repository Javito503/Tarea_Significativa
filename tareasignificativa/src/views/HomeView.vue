<template>
  <div class="home">
    <HelloWorld msg="Welcome to Your Vue.js App"/>
    <CursosDiplomados/>
    <InvestigacionSocial/>
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'
import CursosDiplomados from '@/components/CursosDiplomados.vue'
import InvestigacionSocial from '@/components/InvestigacionSocial.vue';

export default {
  name: 'HomeView',
  components: {
    HelloWorld,
    CursosDiplomados,
    InvestigacionSocial
  }
}
</script>
