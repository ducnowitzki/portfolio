<template>
  <div id="root">
    <nav-bar :activePage="page" @set-page="setPage"></nav-bar>
    <about-me v-if="page === 'about-me'"></about-me>
    <my-cv v-else-if="page === 'my-cv'"></my-cv>
    <contact-me v-else-if="page === 'contact-me'"></contact-me>
    <p v-else>Something went wrong.</p>
  </div>
</template>

<script>
import NavBar from "./components/NavBar.vue";
import AboutMe from "./components/AboutMe.vue";
import MyCv from "./components/MyCv.vue";
import ContactMe from "./components/ContactMe.vue";
export default {
  name: "App",
  components: {
    NavBar,
    AboutMe,
    MyCv,
    ContactMe,
  },
  data() {
    return {
      page: "about-me",
    };
  },
  methods: {
    setPage(page) {
      this.page = page;
    },
  },
};
</script>

<style>
@import url("https://fonts.googleapis.com/css2?family=Varela+Round&display=swap");

#root {
  font-family: "Varela Round", sans-serif;
  text-align: center;
  color: #525d68 !important;
  /* background-color: white; */
  min-height: 100vh;
}
</style>
