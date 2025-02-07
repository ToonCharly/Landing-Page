<template>
  <v-footer dark padless>
    <v-card flat tile class="footer-bg white--text text-center">
      <v-card-text>
        <v-btn
          v-for="(icon, i) in icons"
          :key="i"
          class="mx-4 white--text"
          :href="icon.link"
          target="_blank"
          icon
        >
          <v-icon size="24px">{{ icon.text }}</v-icon>
        </v-btn>
      </v-card-text>

      <v-card-text class="white--text pt-0">
        "El amor de un perro lo cambia todo."
      </v-card-text>

      <v-divider></v-divider>

      <v-card-text class="white--text">
        {{ currentYear }} — <strong>Derechos Reservados</strong>
      </v-card-text>
    </v-card>
  </v-footer>
</template>

<style scoped>
.footer-bg {
  background-color: #d2b48c; /* Color café aplicado al footer */
  width: 100%;
}
</style>

<script>
export default {
  data() {
    return {
      icons: [
        { text: "mdi-facebook", link: "" },
        { text: "mdi-twitter", link: "" },
        { text: "mdi-instagram", link: "" },
      ],
    };
  },
  computed: {
    currentYear() {
      return new Date().getFullYear();
    },
  },
};
</script>
