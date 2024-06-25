<script>
export default {
  props: {
    foods: Array,
  },
};
</script>

<template>
  <div>
    <h1>All Food</h1>
    <div v-for="food in foods" v-bind:key="food.id">
      <h2>{{ food.name }}</h2>
      <h3>{{ food.ethnicity }}</h3>
      <h4>{{ food.time }}</h4>
    </div>
  </div>
</template>

<style></style>
