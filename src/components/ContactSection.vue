<template>
  <section class="pb-8" id="contact">
    <v-container fluid>
      <v-row align="center" justify="center">
        <v-col cols="10">
          <v-row justify="center">
            <v-col cols="12" sm="5">
              <h1 class="font-weight-light display-1">Contáctanos</h1>
              <h3 class="font-weight-light mt-3">
                Si requieres información adicional o asistencia, no dudes en comunicarte con nosotros. 
                Estaremos encantados de atenderte y responder a tus consultas a la brevedad.
              </h3>
              <h3 class="font-weight-light mt-3">
                Tu opinión y preguntas son importantes para nosotros.
              </h3>
              <h3 class="font-weight-light mt-3">
                Phone: +52 (55) 23849-9127
              </h3>
              <h3 class="font-weight-light">
                Email: Dogzline@gmail.com
              </h3>
            </v-col>
            <v-col cols="12" sm="7">
              <v-form ref="form" v-model="valid" :lazy-validation="lazy">
                <v-text-field
                    v-model="name"
                    :rules="nameRules"
                    label="Nombre"
                    required
                ></v-text-field>

                <v-text-field
                    v-model="email"
                    :rules="emailRules"
                    label="Correo"
                    required
                ></v-text-field>

                <v-textarea
                    v-model="textArea"
                    :rules="textAreaRules"
                    label="Mensaje"
                    required
                />

                <v-btn
                    :disabled="!valid"
                    color="primary"
                    :dark="valid"
                    rounded
                    block
                    class="mt-3"
                    @click="submit"
                >
                Enviar
                </v-btn>
              </v-form>
            </v-col>
          </v-row>
        </v-col>
      </v-row>
    </v-container>
    <div class="svg-border-waves text-white">
      <v-img src="~@/assets/img/borderWavesBlue.svg"/>
    </div>
    <v-snackbar
        v-model="snackbar.enabled"
        timeout="3000"
        right
        top
        :color="snackbar.color"
    >
      {{ snackbar.text }}

      <template v-slot:action="{ attrs }">
        <v-btn
            text
            v-bind="attrs"
            @click="snackbar.enabled = false"
        >
          Fechar
        </v-btn>
      </template>
    </v-snackbar>
  </section>
</template>

<style scoped>
#contact {
  background-color: #f4f7f5;
}

.svg-border-waves .v-image {
  position: absolute;
  bottom: 0;
  left: 0;
  height: 3rem;
  width: 100%;
  overflow: hidden;
  filter: brightness(0) saturate(100%) invert(75%) sepia(5%) saturate(0%) hue-rotate(0deg) brightness(85%) contrast(90%);
}

</style>

<script>
export default {
  data: () => ({
    icons: ["fa-facebook", "fa-twitter", "fa-linkedin", "fa-instagram"],
    valid: true,
    name: "",
    nameRules: [
      (v) => !!v || "The name field is required",
      (v) => (v && v.length >= 6) || "The name must be longer than 6 characters",
    ],
    email: "",
    emailRules: [
      (v) => !!v || "The email field is mandatory",
      (v) => /.+@.+\..+/.test(v) || "Email must be valid",
    ],
    textArea: "",
    textAreaRules: [
      (v) => !!v || "The text field is required",
      (v) => (v && v.length >= 10) || "Minimum 10 characters",
    ],
    lazy: false,
    snackbar: {
      enabled: false,
      text: '',
      color: ''
    }
  }),
  methods: {
    submit() {
      /*db.collection("contactData").add({
        name: this.name,
        email: this.email,
        message: this.textArea
      }).then(() => {
        this.snackbar.text = "Mensagem enviada com sucesso"
        this.snackbar.color = "success"
        this.snackbar.enabled = true
      }).catch(() => {
        this.snackbar.text = "Erro ao enviar mensagem"
        this.snackbar.color = "danger"
        this.snackbar.enabled = true
      })*/
    }
  }
};
</script>
