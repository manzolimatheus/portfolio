<template>
  <div class="home">
    <div class="container g-0">
      <div class="row">
        <div class="col-md">
          <!-- Container de apresentação -->
          <Container id="apresentacao">
            <h3>Apresentação</h3>
            <span
              ><ion-icon
                name="information-circle-outline"
                class="text-muted"
              ></ion-icon
            ></span>
            <p>
              Meu nome é Matheus, tenho 17 anos e sou um desenvolvedor de
              software e artista. Sou apaixonado por tecnologia, programação e
              desenhar.
            </p>
            <p>
              <ion-icon name="location" class="text-muted"></ion-icon
              ><span class="ms-2">De Mogi Guaçu - SP</span>
            </p>
            <p>
              <ion-icon name="school" class="text-muted"></ion-icon
              ><span class="ms-2"
                >Cursou o ensino fundamental em
                <strong>Anira Franco de Campos</strong></span
              >
            </p>
            <p>
              <ion-icon name="school" class="text-muted"></ion-icon
              ><span class="ms-2"
                >Cursou o ensino médio em
                <strong>ETEC Euro Albino de Souza</strong></span
              >
            </p>
            <p>
              <ion-icon name="school" class="text-muted"></ion-icon
              ><span class="ms-2"
                >Realizou curso técnico em Desenvolvimento de Sistemas em
                <strong>ETEC Euro Albino de Souza</strong></span
              >
            </p>
            <p>
              <ion-icon name="globe" class="text-muted"></ion-icon>
              <a href="https://github.com/manzolimatheus" target="blank"
                ><span class="ms-2">Github</span></a
              >
            </p>
            <p>
              <ion-icon name="globe" class="text-muted"></ion-icon>
              <a href="https://www.behance.net/manzolimatheus" target="blank"
                ><span class="ms-2">Behance</span></a
              >
            </p>
            <p>
              <ion-icon name="globe" class="text-muted"></ion-icon>
              <a
                href="https://www.linkedin.com/in/manzolimatheus"
                target="blank"
                ><span class="ms-2">Linkedin</span></a
              >
            </p>
          </Container>
          <!-- Container de habilidades -->
          <Container>
            <h3>Habilidades</h3>
            <br />
            <div id="habilidades" class="row g-1">
              <div
                class="col-md-3"
                v-for="(habilidade, index) in habilidades"
                :key="index"
              >
                <p class="habilidade">
                  <ion-icon
                    :name="habilidade.icone"
                    class="text-muted"
                  ></ion-icon
                  ><span class="ms-2">{{ habilidade.nome }}</span>
                </p>
              </div>
            </div>
          </Container>
          <!-- Container de habilidades futuras -->
          <Container>
            <h3>O que pretendo aprender futuramente?</h3>
            <br />
            <div id="habilidades" class="row g-1">
              <div
                class="col-md-4"
                v-for="(habilidade, index) in habilidades_futuras"
                :key="index"
              >
                <p class="habilidade">
                  <ion-icon
                    :name="habilidade.icone"
                    class="text-muted"
                  ></ion-icon
                  ><span class="ms-2">{{ habilidade.nome }}</span>
                </p>
              </div>
            </div>
          </Container>
        </div>
        <div class="col-md">
          <Container v-for="(post, index) in posts" :key="index">
            <div class="row">
              <div class="col-2">
                <img
                  src="https://avatars.githubusercontent.com/u/85998383?v=4"
                  alt="Imagem de perfil"
                  class="rounded-circle"
                  style="width: 50px"
                />
              </div>
              <div class="col-10">
                <h5>Matheus Manzoli</h5>
                <p class="text-muted">
                  <ion-icon name="globe"></ion-icon
                  ><span class="ms-2">{{ post.date || "Não definido" }}</span>
                </p>
              </div>
              <p class="text">{{ post.text || null }}</p>
              <a
                :href="post.link"
                v-if="post.link != null"
                class="text-decoration-none"
                >{{ post.link }}</a
              >
              <img
                :src="post.image"
                alt="Imagem da postagem"
                v-if="post.image != null"
                class="w-100 rounded mt-1"
              />
            </div>
          </Container>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Container from "@/components/Container.vue";

export default {
  name: "Home",
  components: {
    Container,
  },
  data() {
    return {
      habilidades: [
        {
          nome: "HTML",
          icone: "code",
        },
        {
          nome: "CSS",
          icone: "code",
        },
        {
          nome: "Javascript",
          icone: "code",
        },
        {
          nome: "PHP",
          icone: "code",
        },
        {
          nome: "Python",
          icone: "code",
        },
        {
          nome: "Bootstrap",
          icone: "code",
        },
        {
          nome: "Laravel",
          icone: "code",
        },
        {
          nome: "Vue.js",
          icone: "code",
        },
        {
          nome: "MySQL",
          icone: "code",
        },
        {
          nome: "Wordpress",
          icone: "code",
        },
        {
          nome: "Photoshop",
          icone: "color-palette",
        },
        {
          nome: "Gimp",
          icone: "color-palette",
        },
        {
          nome: "Figma",
          icone: "color-palette",
        },
        {
          nome: "UI",
          icone: "color-palette",
        },
        {
          nome: "Arte digital",
          icone: "color-palette",
        },
        {
          nome: "Windows",
          icone: "cube",
        },
        {
          nome: "Ubuntu Linux",
          icone: "cube",
        },
        {
          nome: "Dedicado",
          icone: "heart",
        },
        {
          nome: "Criativo",
          icone: "heart",
        },
        {
          nome: "Inglês",
          icone: "language",
        },
      ],
      habilidades_futuras: [
        {
          nome: "Blender",
          icone: "color-palette",
        },
        {
          nome: "Node.js",
          icone: "code",
        },
        {
          nome: "Dev. Jogos",
          icone: "code",
        },
        {
          nome: "Golang",
          icone: "code",
        },
      ],
      posts: [
        {
          text: "Bem-vindo ao meu portfólio/Currículo interativo! Abaixo você poderá ler uma linha do tempo sobre acontecimentos recentes.",
          date: "Dezembro de 2021",
          image: "https://media0.giphy.com/media/xT8qBhrlNooHBYR9f2/giphy.gif",
        },
        {
          text: "TCC finalizado com sucesso! Foi uma longa jornada até chegar aqui, tudo o que nos resta é orgulho e satisfação! Você pode visitar nosso TCC no link abaixo.",
          link: "http://helphere.online/",
          date: "Dezembro de 2021",
          image: "/img/tcc.jpeg",
        },
        {
          text: "Comecei a estudar Vue.js!",
          date: "Agosto de 2021",
          image:
            "https://community-cdn-digitalocean-com.global.ssl.fastly.net/variants/snN3rbgKF7McfuiQAKcoLWMn/035575f2985fe451d86e717d73691e533a1a00545d7230900ed786341dc3c882",
        },
        {
          text: "Início do desenvolvimento do TCC utilizando Laravel e Bootstrap",
          date: "Abril de 2021",
          image: "/img/screenshot_tcc.png",
        },
        {
          text: "Comecei a estudar Laravel 8!",
          date: "Março de 2021",
          image: "https://mazer.dev/wp-content/uploads/2021/03/laravel-8.png",
        },
        {
          text: "Durante 2020 estudei muita coisa, entre elas, PHP, MySQL, Python e C#",
          date: "Dezembro de 2020",
          image:
            "https://daneshjooyar.com/wp-content/uploads/2021/01/sqlinphp.png",
        },
        {
          text: "Durante 2019 tive a base de algoritmos, estruturas de dados e lógica de programação. Em seguida passamos a experimentar algoritmos no visualG, ao mesmo tempo que aprendíamos HTML, CSS, Javascript e Bootstrap, assim como fazer uma análise completa das necessidades de um cliente e moldar a estrutura do banco de dados.",
          date: "Dezembro de 2019",
          image:
            "https://upload.wikimedia.org/wikipedia/commons/a/aa/Fluxogranma02.gif",
        },
        {
          text: "Entrei na ETEC, uma escola técnica de ensino médio com entrada via processo seletivo.",
          date: "Fevereiro de 2019",
          image:
            "https://www.gazetaguacuana.com.br/wp-content/uploads/2017/02/297_Alunas-ETEC-Faculdade.jpg",
        },
      ],
    };
  },
};
</script>

<style scoped>
#apresentacao a {
  text-decoration: none;
}

.habilidade {
  border-radius: 20px;
  border: 1px solid #4b4b4b;
  padding: 2%;
  margin: 2%;
  width: 100%;
}

.text {
  white-space: pre-line;
  text-align: justify;
}
</style>
