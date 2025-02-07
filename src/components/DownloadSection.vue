<template>
  <section id="download">
    <v-container fluid>
      <v-row align="center" justify="center">
        <v-col cols="10">
          <v-row align="center" justify="center">
            <v-col sm="4" class="hidden-xs-only">
              <v-img src="@/assets/img/playg.png" class="d-block ml-auto mr-auto" max-width="300px" />
            </v-col>
            <v-col cols="12" sm="8" class="white--text text-left">
              <h1 class="font-weight-light display-2 mb-2">Descargalo ahora!!</h1>
              <h1 class="font-weight-light">
                Facilita a tu perro encontrar una pareja compatible de manera rápida y segura. 
                Con nuestra app, el proceso es sencillo y confiable.
              </h1>
              <v-btn rounded outlined href="https://play.google.com/store/apps" target="_blank" large color="white" class="mt-4">
                <!-- <v-icon class="mr-2">
                  mdi-github
                </v-icon> -->
                Descargar
              </v-btn>
            </v-col>
          </v-row>
        </v-col>
      </v-row>
    </v-container>
  </section>
</template>

<style scoped>
#download {
  background-image: url("~@/assets/img/perro.jpg");
  background-attachment: fixed;
  background-repeat: no-repeat;
  background-size: cover;
  background-position: center;
  height: 500px;
}

#download .container,
#download .row {
  height: 100%;
}
</style>