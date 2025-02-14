<template>
  <section id="about">
    <v-container fluid>
      <v-row align="center" justify="center">
        <v-col cols="10">
          <v-row align="center" justify="center">
            <v-col cols="12" md="7">
              <h1 class="font-weight-light display-2">Sobre Nosotros</h1>
              <h1 class="font-weight-light display-1 mb-3">
                Conectamos perros y dueños de forma fácil y segura
              </h1>
              <v-row>
                <v-col cols="12" class="d-flex align-center">
                  <v-img
                    src="@/assets/img/icons8-perro-100.png"
                    max-width="60px"
                    class="mr-4"
                  />
                  <p class="text-justify">
                    Facilitamos la búsqueda de compañeros para tu perro, 
                    ya sea para apareamiento selectivo o simplemente para hacer nuevos amigos.
                  </p>
                </v-col>
                <v-col cols="12" class="d-flex align-center">
                  <v-img
                    src="@/assets/img/icons8-chats-96.png"
                    max-width="60px"
                    class="mr-4"
                  />
                  <p class="text-justify">
                    Chatea con otros dueños de perros y coordina encuentros de manera rápida y sencilla.
                  </p>
                </v-col>
                <v-col cols="12" class="d-flex align-center">
                  <v-img
                    src="@/assets/img/icons8-cohete-100.png"
                    max-width="60px"
                    class="mr-4"
                  />
                  <p class="text-justify">
                    Nuestro algoritmo avanzado te ayuda a encontrar coincidencias perfectas según raza, ubicación e intereses.
                  </p>
                </v-col>
              </v-row>
            </v-col>
            <v-col cols="12" md="5" class="d-none d-md-flex">
              <v-img
                src="@/assets/img/ill1.svg"
                class="d-block ml-auto mr-auto"
                max-width="400px"
              />
            </v-col>
          </v-row>
        </v-col>
      </v-row>
    </v-container>
  </section>
</template>



<style scoped>
#about {
  background-color: #f4f7f5;
}
</style>

