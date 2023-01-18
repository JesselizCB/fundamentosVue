<template>
  <v-container>
    <v-row class="justify-center">
      <v-col cols="12" sm="6" md="8">
        <v-text-field
          v-model="question"
          label="Pregunta"
          placeholder="Hazme una pregunta"
        ></v-text-field>
        <p>Recuerda terminar con un signo de interrogación (?)</p>
        <div>
          <h1>{{ question }}</h1>
          <h2>Si, No... Quiza</h2>

          <div class="pt-8">
            <v-img
              src="https://cdn.vuetifyjs.com/images/parallax/material2.jpg"
              gradient="to top right, rgba(100,115,201,.33), rgba(25,32,72,.7)"
            ></v-img>
          </div>
        </div>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  data() {
    return {
      question: "",
      isValidQuestion: false,
    };
  },
  created () {
    this.promesa(false);
  },
  watch: {
    question(value, oldValue) {
      if (!value.includes("?")) return;
      this.isValidQuestion = true;
      //TODO: Realizar la peticion de la API: https://yesno.wtf/api
    },
  },
  methods: {

    promesa(param) {
      console.log('Inicio')
      new Promise((resolve, reject) => {
        console.log('Cuerpo de la promesa')
        param ? resolve('La promsa se resolvio correctamente') : reject('La promesa fue rechazada')
        // resolve('La promsa se resolvio correctamente')
        
      }).then(console.log).catch(console.log)

      console.log('Fin')
    },

    getAnswer() {
      console.log('in get answer')
    }
  },
};
</script>

<style lang="scss" scoped></style>
