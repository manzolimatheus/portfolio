<template>
  <nav class="shadow sticky-top bg-white">
    <span></span>
    <div id="nav" class="text-center">
      <router-link to="/"
        ><ion-icon name="home-outline"></ion-icon
      ></router-link>
      <router-link to="/projects"
        ><ion-icon name="bulb-outline"></ion-icon
      ></router-link>
      <router-link to="/arts"
        ><ion-icon name="color-palette-outline"></ion-icon
      ></router-link>
    </div>
    <span></span>
  </nav>
</template>

<script>
export default {
  name: "Navbar",
};
</script>

<style>
nav {
  display: grid;
  grid-template-columns: 20% 60% 20%;
  height: fit-content;
}

nav a {
  padding: 0 4% 0 4%;
  font-size: 24pt;
}

nav a:hover {
  border-radius: 20px;
  transition: 0.5s;
  background-color: #0d6efd;
  color: white;
}
</style>
