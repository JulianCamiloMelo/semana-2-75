<template>
  <div>
    <div v-if="member.codigo % 2 == 0" class="card border-info text-black">
      <div class="d-flex justify-content-center p-2">
        <img
          v-bind:src="require('../assets/' + member.image)"
          alt="Imagen del Integrante"
        />
      </div>
      <div class="card-body">
        <h5 class="card-title">{{ member.nombre }}</h5>
        <p class="card-text">Código: {{ member.codigo }}</p>
        <p class="card-text">Rol: {{ member.rol }}</p>
        <br />
        <p class="card-text">{{ member.descripcion }}</p>
      </div>
    </div>
    <div v-else class="card text-white bg-dark">
      <div class="d-flex justify-content-center p-2">
        <img
          v-bind:src="require('../assets/' + member.image)"
          alt="Imagen del Integrante"
        />
      </div>
      <div class="card-body">
        <h5 class="card-title">{{ member.nombre }}</h5>
        <p class="card-text">Código: {{ member.codigo }}</p>
        <p class="card-text">Rol: {{ member.rol }}</p>
        <br />
        <p class="card-text">{{ member.descripcion }}</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "TeamCard",
  props: ["member"],
};
</script>
