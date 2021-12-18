<template>
  <Navbar />
  <Header />
  <router-view />
</template>

<script>
import Navbar from "@/components/Navbar.vue";
import Header from "@/components/Header.vue";

export default {
  components: {
    Navbar,
    Header,
  },
};
</script>

<style>
body {
  background-color: #f5f5f5;
}

/* Scrollbar */
/* width */
::-webkit-scrollbar {
  width: 10px;
}
/* Track */
::-webkit-scrollbar-track {
  background: #f1f1f1;
}
/* Handle */
::-webkit-scrollbar-thumb {
  background: #bbbbbb;
  border-radius: 10px;
}
/* Handle on hover */
::-webkit-scrollbar-thumb:hover {
  background: #555;
}
</style>
