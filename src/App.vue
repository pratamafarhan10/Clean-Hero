<template>
  <navbar :class="{ 'bg-white': scrollPosition > 50 }"></navbar>
  <section id="home" class="h-screen flex flex-col">
    <div class="container lg:px-14 flex-grow mx-auto flex justify-items-center">
      <home></home>
    </div>
  </section>

  <section id="games" class="h-screen flex flex-col">
    <div class="container lg:px-14 flex-grow mx-auto flex items-center">
      <game></game>
    </div>
  </section>

  <section id="about" class="h-screen flex flex-col">
    <div class="container mx-auto lg:px-14 flex-grow flex items-center">
      <about-card></about-card>
    </div>
  </section>

  <section id="contact" class="border-t-2">
    <footer-page></footer-page>
  </section>
</template>

<script>
import Navbar from "./components/ui/Navbar.vue";
import FooterPage from './components/ui/Footer.vue';
import Home from "./components/pages/Home.vue";
import Game from "./components/pages/Game.vue";
import AboutCard from "./components/ui/card/AboutCard.vue";

export default {
  components: {
    Navbar,
    FooterPage,
    Home,
    Game,
    AboutCard,
  },
  data() {
    return {
      scrollPosition: null,
    };
  },
  methods: {
    updateScroll() {
      this.scrollPosition = window.scrollY;
    },
  },
  mounted() {
    document.title = "Clean Hero";
    window.addEventListener("scroll", this.updateScroll);
  },
};
</script>

<style>
html {
  scroll-behavior: smooth;
}

body {
  background: url("./assets/fullbg.svg") no-repeat;
  background-size: cover;
}
</style>