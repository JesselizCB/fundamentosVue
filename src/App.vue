<template>
  <v-app>
    <v-app-bar app color="deep-purple lighten-2" dark class="d-flex justify-center">
      <div class="d-flex align-center">
        <h2>TODO APP</h2>
      </div>
    </v-app-bar>

    <v-main>
      <!-- <Counter/> -->
      <Todo />
    </v-main>
  </v-app>
</template>

<script>
import Counter from "./components/Counter.vue";
import Todo from "./components/Todo";

export default {
  name: "App",

  components: {
    Counter,
    Todo,
  },

  data: () => ({
    //
  }),
};
</script>
