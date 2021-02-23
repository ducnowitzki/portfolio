<template>
  <b-container align="center" class="contact">
    <b-card title="Feel free to contact me" class="mb-3 mb-md-4 mx-md-5">
      <b-row align-h="center" class="flexrow">
        <a href="mailto:minhduc.ng97@gmail.com">
        <b-avatar
          :src="require('../assets/mail-blue.png')"
          rounded=""
          size="3rem"
          class="rounded-icon mx-3"
        ></b-avatar></a>
        <a href="https://github.com/ducnowitzki/">
          <b-avatar
            :src="require('../assets/github.png')"
            rounded="lg"
            size="3rem"
            class="mx-3"
          ></b-avatar
        ></a>
        <a href="https://www.linkedin.com/in/minh-duc-nguyen-6a50b6204/">
          <b-avatar
            :src="require('../assets/linkedin-icon-dark.svg')"
            rounded="lg"
            size="3rem"
            class="mx-3"
          ></b-avatar
        ></a>
      </b-row>
    </b-card>
  </b-container>
</template>

<style scoped>
/* .contact {
  padding-top: 5%;
} */

.badge-secondary {
  background-color: transparent;
}

.rounded-icon {
  border-radius: 15px !important;
}
</style>
