<template>
  <div id="header">
    <Container class="text-center header mt-0">
      <img
        src="https://camo.githubusercontent.com/64f467f8e119aa9d921235de665fdc9dbbf0b6eb7da1c1525385eda96660acdc/68747470733a2f2f692e696d6775722e636f6d2f7630545a3439342e706e67"
        alt="Capa"
        class="w-100 rounded-bottom"
      />
      <img
        src="https://avatars.githubusercontent.com/u/85998383?v=4"
        alt="Foto de perfil"
        class="rounded-circle profile-photo"
      />
      <h1>Matheus Manzoli</h1>
      <p class="text-muted">Desenvolvedor de software e artista</p>
      <q>Quem tenta pode falhar, mas quem não tenta, já falhou</q>
      <hr />
      <div class="row">
        <div class="col">
          <h5><router-link to="/">Sobre</router-link></h5>
        </div>
        <div class="col">
          <h5><router-link to="/projects">Projetos</router-link></h5>
        </div>
        <div class="col">
          <h5><router-link to="/arts">Artes</router-link></h5>
        </div>
      </div>
    </Container>
  </div>
</template>

<script>
import Container from "@/components/Container.vue";

export default {
  name: "Header",
  components: {
    Container,
  },
};
</script>

<style>
.profile-photo {
  margin-top: -5%;
  width: 250px;
  border: 5px solid white;
}

.header a {
  color: #252525;
  text-decoration: none;
}

.header a:hover {
  transition: 0.3s;
  color: #0d6efd;
}
</style>
