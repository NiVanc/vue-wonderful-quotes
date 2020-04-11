<template>
  <div class="container">
    <app-quotes :quotes="quotes"></app-quotes>
  </div>
</template>

<script>
import QuoteGrid from "./components/QuoteGrid.vue";

export default {
  data() {
    return {
      quotes: ["A first quote to see something"],
      maxQuotes: 10
    };
  },
  components: {
    "app-quotes": QuoteGrid
  }
};
</script>

<style>
</style>
