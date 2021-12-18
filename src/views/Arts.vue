<template>
  <div id="arts">
    <Container class="mt-3">
      <p>
        <span class="h3">Artes</span
        ><span class="ms-3"
          ><a
            href="https://www.behance.net/manzolimatheus"
            class="text-decoration-none"
            target="blank"
            >Ver mais</a
          ></span
        >
      </p>
      <div class="row m-1">
        <div class="col-md-3 g-0" v-for="index in 20" :key="index">
          <img
            :src="`https://raw.githubusercontent.com/manzolimatheus/portfolio-images/main/desenhos/img${index}.png`"
            alt="Arte"
            class="w-100 art-image"
            @click="
              openModal(
                `https://raw.githubusercontent.com/manzolimatheus/portfolio-images/main/desenhos/img${index}.png`
              )
            "
            data-bs-toggle="modal"
            data-bs-target="#modal"
          />
        </div>
      </div>
    </Container>
    <Container class="mt-3">
      <p>
        <span class="h3">Logos</span
        ><span class="ms-3"
          ><a
            href="https://www.behance.net/manzolimatheus"
            class="text-decoration-none"
            target="blank"
            >Ver mais</a
          ></span
        >
      </p>
      <div class="row m-1">
        <div class="col-md-3 g-0" v-for="index in 3" :key="index">
          <img
            :src="`https://raw.githubusercontent.com/manzolimatheus/portfolio-images/main/logos/${index}.jpg`"
            alt="Arte"
            class="w-100 art-image"
            @click="
              openModal(
                `https://raw.githubusercontent.com/manzolimatheus/portfolio-images/main/logos/${index}.jpg`
              )
            "
            data-bs-toggle="modal"
            data-bs-target="#modal"
          />
        </div>
      </div>
    </Container>
    <Container class="mt-3">
      <p>
        <span class="h3">Protótipos</span
        ><span class="ms-3"
          ><a
            href="https://www.behance.net/manzolimatheus"
            class="text-decoration-none"
            target="blank"
            >Ver mais</a
          ></span
        >
      </p>
      <div class="row m-1">
        <div class="col-md-3 g-0" v-for="index in 11" :key="index">
          <img
            :src="`https://raw.githubusercontent.com/manzolimatheus/portfolio-images/main/prototipos/${index}.png`"
            alt="Arte"
            class="w-100 art-image"
            @click="
              openModal(
                `https://raw.githubusercontent.com/manzolimatheus/portfolio-images/main/prototipos/${index}.png`
              )
            "
            data-bs-toggle="modal"
            data-bs-target="#modal"
          />
        </div>
      </div>
    </Container>
    <!-- Modal -->
    <div class="modal" id="modal" tabindex="-1">
      <div class="modal-dialog">
        <div class="modal-content">
          <div class="modal-header">
            <h5 class="modal-title">Imagem</h5>
            <button
              type="button"
              class="btn-close"
              data-bs-dismiss="modal"
              aria-label="Close"
            ></button>
          </div>
          <div class="modal-body">
            <img :src="src" alt="Arte" class="w-100" />
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Container from "@/components/Container";

export default {
  name: "Arts",
  components: {
    Container,
  },
  data() {
    return {
      src: "",
    };
  },
  methods: {
    openModal(src) {
      this.src = src;
    },
  },
};
</script>

<style>
.art-image {
  width: 200px;
  height: 200px;
  object-fit: cover;
}

@media (max-width: 768px) {
  .col-md-3 {
    flex: 0 0 auto;
    width: 50%;
  }

  .art-image {
    width: 100%;
    height: 200px;
    object-fit: cover;
  }
}

.art-image:hover {
  filter: brightness(0.8);
  cursor: pointer;
}
</style>
