<template>
  <div>
    <div class="d-flex flex-column align-center pt-10">
      <h2>Counter!</h2>
      <p>{{ contador }}<sup>2</sup> = {{ squareCounterComputed }}</p>
      <p>{{ contador }}<sup>2</sup> = {{ squareCounterComputed }}</p>
      <p>{{ contador }}<sup>2</sup> = {{ squareCounterComputed }}</p>
      <p>{{ contador }}<sup>2</sup> = {{ squareCounterComputed }}</p>
      <p>{{ contador }}<sup>2</sup> = {{ squareCounterComputed }}</p>
      <p>{{ contador }}<sup>2</sup> = {{ squareCounterComputed }}</p>
      <div>
        <v-btn class="mx-2" fab dark small color="primary" @click="decrease">
          <v-icon dark> mdi-minus </v-icon>
        </v-btn>
        <v-btn class="mx-2" fab dark small color="purple" @click="increse">
          <v-icon dark> mdi-plus </v-icon>
        </v-btn>

        <!-- <button class="btn-inicial" @click="increse">+1</button>
        <button class="btn-inicial" @click="decrease">-1</button> -->
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Counter",
  data() {
    return {
      contador: 10,
    };
  },
  methods: {
    squareCounter() {
      console.log("in square method");
      return this.contador * this.contador;
    },
    increse() {
      this.contador++;
    },

    decrease() {
      this.contador--;
    },
  },
  computed: {
    squareCounterComputed() {
      console.log("in computed");
      return this.contador * this.contador;
    },
  },
};
</script>

<style scoped>
.btn-inicial {
  border: 1px solid white;
  border-radius: 5px;
  margin: 0 5px;
  color: white;
  cursor: pointer;
  padding: 5px 15px;
  background-color: rgb(87, 165, 87);
}
</style>
