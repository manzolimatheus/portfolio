<template>
  <div id="projects">
    <Container>
      <p>
        <span class="h3">Projetos em destaque</span
        ><span class="ms-3"
          ><a
            href="https://github.com/manzolimatheus"
            class="text-decoration-none"
            target="blank"
            >Ver mais</a
          ></span
        >
      </p>
    </Container>
    <Container v-for="project in projects" :key="project.id" class="mt-3">
      <strong>{{ project.name }}</strong>
      <span class="text-success ms-3"
        ><ion-icon name="code"></ion-icon
        ><span class="ms-2">{{ project.language }}</span></span
      >
      <p class="text-muted">{{ project.description }}</p>
      <a
        :href="project.link"
        class="text-decoration-none"
        target="blank"
        v-if="project.link !== ''"
      >
        <p>
          <ion-icon name="globe"></ion-icon><span class="ms-2">Visitar</span>
        </p>
      </a>
      <img
        :src="project.image"
        alt="Imagem do projeto"
        class="w-100 rounded"
        v-if="project.image !== ''"
      />
    </Container>
  </div>
</template>

<script>
import Container from "@/components/Container.vue";

export default {
  name: "Projects",
  components: {
    Container,
  },
  data() {
    return {
      projects: [
        {
          name: "Help Here!",
          description:
            "Help Here! é uma aplicação WEB que visa auxiliar os usuários a encontrar doações em dinheiro via PIX.",
          language: "Laravel",
          link: "http://helphere.online/",
          image: "/img/screenshot_tcc.png",
        },
        {
          name: "Crud de produtos",
          description:
            "Crud de produtos, com uma API feita com Laravel e frontend feito com Vue.js, contém sistema de autenticação via token, painel de administração, paginação e pedidos.",
          language: "Laravel, Vue.js",
          link: "",
          image:
            "https://camo.githubusercontent.com/0e9f1f21a5606d267282cae49dbe626fa2d7b4c3c4750286bf553418f50c1e1c/68747470733a2f2f692e696d6775722e636f6d2f50667a713078312e706e67",
        },
        {
          name: "Site de sociologia",
          description:
            "Site para apresentar temas em debate na matéria de sociologia, nesse projeto fiquei responsável pelo desenvolvimento do site para apresentar aos estudantes da escola.",
          link: "https://penguinweather.vercel.app/",
          language: "Vue.js",
          image: "https://i.imgur.com/JLggXC7.png",
        },
        {
          name: "Penguinweather",
          description:
            "Este site tem como objetivo mostrar dados do tempo de um determinado local, como temperatura, umidade, vento, etc.",
          link: "https://socio-site.vercel.app/",
          language: "Vue.js",
          image:
            "https://camo.githubusercontent.com/9294b99832bfe1b4fd3624abc58c37c7c3362ab0f7f40ff9aea17402028af2f2/68747470733a2f2f692e696d6775722e636f6d2f76305a57524f6e2e6a7067",
        },
      ],
    };
  },
};
</script>

<style></style>
