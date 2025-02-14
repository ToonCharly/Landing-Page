<template>
  <section id="team" class="py-5">
    <v-container>
      <v-row align="center" justify="center">
        <v-col cols="12" class="text-center">
          <h2 class="display-2 font-weight-bold mb-4">Nuestro Equipo</h2>
          <p class="font-weight-light">
            Conoce a las personas detrás de Dogzline.
          </p>
        </v-col>
        <v-col
          cols="12"
          sm="4"
          class="text-center"
          v-for="(member, index) in team"
          :key="index"
        >
          <v-hover v-slot:default="{ hover }">
            <v-card
              class="card"
              shaped
              :elevation="hover ? 10 : 4"
              :class="{ up: hover }"
            >
              <v-img
                :src="member.img"
                max-width="100px"
                class="d-block ml-auto mr-auto"
                :class="{ 'zoom-efect': hover }"
              ></v-img>
              <h1 class="font-weight-regular">{{ member.name }}</h1>
              <h4 class="font-weight-regular subtitle-1">
                {{ member.role }}
              </h4>
              <v-card-text>{{ member.description }}</v-card-text>
            </v-card>
          </v-hover>
        </v-col>
      </v-row>
    </v-container>
  </section>
</template>

<script>
export default {
  data() {
    return {
      team: [
        {
          img: require("@/assets/img/esmorto.jpg"),
          name: "Rodrigo Esmorto",
          role: "CEO & Fundador",
          description: "Banco de la UTM.",
        },
        {
          img: require("@/assets/img/sergio.jpg"),
          name: "Sergio España",
          role: "CTO",
          description: "Puede actuar en caidas (se cae de verdad).",
        },
        {
          img: require("@/assets/img/carlos.jpg"),
          name: "Carlos Pech",
          role: "CMO",
          description: "Maestro Pokemon.",
        },
      ],
    };
  },
};
</script>

<style scoped>
.card {
  min-height: 300px;
  padding: 10px;
  transition: 0.5s ease-out;
}

.card .v-image {
  margin-bottom: 15px;
  transition: 0.75s;
}

.card h1 {
  margin-bottom: 10px;
}

.zoom-efect {
  transform: scale(1.1);
}

.up {
  transform: translateY(-20px);
  transition: 0.5s ease-out;
}
</style>