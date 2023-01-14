<template>
  <div>
    <h2>Counter!</h2>
    <p>{{contador}}<sup>2</sup> = {{ squareCounterComputed }}</p>
    <p>{{contador}}<sup>2</sup> = {{ squareCounterComputed }}</p>
    <p>{{contador}}<sup>2</sup> = {{ squareCounterComputed }}</p>
    <p>{{contador}}<sup>2</sup> = {{ squareCounterComputed }}</p>
    <p>{{contador}}<sup>2</sup> = {{ squareCounterComputed }}</p>
    <p>{{contador}}<sup>2</sup> = {{ squareCounterComputed }}</p>
    <div>
      <button @click="increse">+1</button>
      <button @click="decrease">-1</button>
    </div>

  </div>
  
</template>

<script>
export default {
  name: "Counter",
    data() {
      return {
        contador: 10
      }
  },
  methods: {
    squareCounter() {
      console.log('in square method')
      return this.contador * this.contador
    },
    increse() {
      this.contador++;
    },

    decrease() {
      this.contador--;
    }

  },
  computed: {
    squareCounterComputed() {
      console.log('in computed')
      return this.contador * this.contador
    }
  }
    
  }
</script>

<style scoped>
button {
  border: 1px solid white;
  border-radius: 10px;
  margin:0 5px;
  color:white;
  cursor:pointer;
  padding: 5px 15px;
  background-color:rgb(87, 165, 87)
}
</style>