<template>
  <div id="app">
    <!-- Llamar banner -->
    <top-banner></top-banner>

    <!-- Llamar api -->
    <section id="api" class="api">
      <div class="container-fluid">
        <section-api></section-api>
      </div>
    </section>

    <!-- Llamar los miembros -->
    <section id="team" class="miembros">
      <div class="container-fluid">
        <div class="row justify-content-center mb-5">
          <div class="col mt-5" v-for="(item, index) of team" :key="index">
            <team-card v-bind:member="item"></team-card>
          </div>
        </div>
      </div>
    </section>

    <page-footer></page-footer>
  </div>
</template>

<script>
import TeamCard from "./components/TeamCard.vue";
import PageFooter from "./components/PageFooter.vue";
import SectionApi from "./components/SectionApi.vue";
import TopBanner from "./components/TopBanner.vue";

export default {
  name: "App",
  components: {
    TopBanner,
    SectionApi,
    TeamCard,
    PageFooter,
  },
  data() {
    return {
      team: [
        {
          codigo: 1,
          nombre: "Sandra Palacio H",
          descripcion:
            "Ingeniera Electricista de la Universidad Nacional. Pasatiempos: Viajar, practicar baloncesto, nadar e ir a la playa.",
          rol: "Desarrollador FrontEnd",
          image: "smph2.png",
        },
        {
          codigo: 2,
          nombre: "Julian Melo S",
          descripcion:
            "Desarrollador de Software, Ingeniería de Sistemas. Pasatiempos: Leer, jugar futbol y practicar ciclismo de montaña.",
          rol: "Desarrollador BackEnd",
          image: "JuanC200.jpg",
        },
        {
          codigo: 3,
          nombre: "Teobaldo Manjarres",
          descripcion:
            "Ingeniería Electrónica, Universidad Nacional. Pasatiempos: Matemáticas, Lectura, Videojuegos y Deportes.",
          rol: "Desarrollador BackEnd",
          image: "Teo200.jpg",
        },
        {
          codigo: 4,
          nombre: "Milton García G",
          descripcion:
            "Arquitecto de la Universidad Nacional. Pasatiempos: Practicar Deportes, jugar baloncesto, cursos en línea.",
          rol: "Tester",
          image: "Milton200.jpg",
        },
        {
          codigo: 5,
          nombre: "Integrante 5",
          descripcion: "Universidad",
          rol: "Desarrollador",
          image: "men.jpg",
        },
      ]
    };
  },
};
</script>

