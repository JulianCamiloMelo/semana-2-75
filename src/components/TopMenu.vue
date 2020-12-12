<template>
  <nav class="navbar navbar-expand-lg sticky-top navbar-dark bg-dark">
    <a class="navbar-brand">
      <img
        src="../assets/sun.png"
        width="30 "
        height="30"
        class="d-inline-block align-top"
        alt=" "
        loading="lazy "
      />
      Energía Solar en Colombia
    </a>
    <div class="collapse navbar-collapse justify-content-end" id="navbarNav ">
      <ul class="navbar-nav">
        <li class="nav-item active">
          <a class="nav-link" href="# "
            >Inicio<span class="sr-only">(current)</span></a
          >
        </li>
        <li class="nav-item">
          <a class="nav-link" href="#api">API IMDb</a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="#team">Miembros</a>
        </li>
      </ul>
    </div>
  </nav>
</template>
<script>
export default {
  name: "TopMenu",
};
</script>