<template>
  <b-navbar class="flex-column flex-md-row" sticky type="light" toggleable="sm">
    <b-navbar-brand class="mr-0 mr-md-2" href="#">MDN</b-navbar-brand>

    <b-navbar-nav class="flex-row flex-column-md">
      <b-nav-item class="mx-3 mx-md-0" :active="aboutMe" @click="setPage('about-me')"
        >About Me</b-nav-item
      >
      <b-nav-item class="mx-3 mx-md-0" :active="myCv" @click="setPage('my-cv')">CV</b-nav-item>
      <b-nav-item class="mx-3 mx-md-0" :active="contactMe" @click="setPage('contact-me')"
        >Contact</b-nav-item
      >
    </b-navbar-nav>
    <!-- <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>
    <b-collapse id="nav-collapse" is-nav>
      <b-navbar-nav>
        <b-nav-item :active="aboutMe" @click="setPage('about-me')"
          >About Me
        </b-nav-item>
        <b-nav-item :active="myCv" @click="setPage('my-cv')">CV</b-nav-item>
        <b-nav-item :active="contactMe" @click="setPage('contact-me')"
          >Contact</b-nav-item
        >
      </b-navbar-nav>
    </b-collapse> -->
  </b-navbar>
</template>

<script>
export default {
  props: ["activePage"],
  computed: {
    aboutMe() {
      return this.activePage === "about-me" ? true : false;
    },
    myCv() {
      return this.activePage === "my-cv" ? true : false;
    },
    contactMe() {
      return this.activePage === "contact-me" ? true : false;
    },
  },
  methods: {
    setPage(page) {
      this.$emit("set-page", page);
    },
  },
};
</script>

<style scoped>
/* #navbar {
  background-color: #06BC9B !important;
} */

.navbar {
  background-color: white;
  border-bottom: lightgray solid 1px;
}


.navbar-brand,
.nav .navbar-brand:hover {
  color: #06bc9b !important;
  font-size: xx-large;
}

/* .navbar-nav {
  display: inline-block;
}

.navbar-nav > li {
    display: inline-block;
} */

.navbar-nav a {
  color: #525d68 !important;
  font-size: medium;
}

.navbar-nav a:hover {
  color: #16c0a1 !important;
}

.navbar-nav a.active {
  /* font-weight: bold; */
  color: #06bc9b !important;
  /* border-bottom: #06bc9b solid 0.25rem; */
}
</style>
