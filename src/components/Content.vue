<script>
import FoodsIndex from "./FoodsIndex.vue";
import axios from "axios";

export default {
  components: {
    FoodsIndex,
  },
  data: function () {
    return {
      foods: [],
    };
  },
  created() {
    this.handleIndexFoods();
  },
  methods: {
    handleIndexFoods: function () {
      axios.get("http://localhost:3000/foods.json").then((response) => {
        console.log("foods index", response);
        this.foods = response.data;
      });
    },
  },
};
</script>

<template>
  <main>
    <FoodsIndex v-bind:foods="foods" />
  </main>
</template>

<style></style>
