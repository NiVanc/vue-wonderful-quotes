<template>
  <div class="container">
    <app-new-quote @quoteAdded="quotes.push($event)"></app-new-quote>
    <app-quotes :quotes="quotes"></app-quotes>
  </div>
</template>

<script>
import QuoteGrid from "./components/QuoteGrid.vue";
import NewQuote from "./components/NewQuote.vue";

export default {
  data() {
    return {
      quotes: ["A first quote to see something"],
      maxQuotes: 10
    };
  },
  components: {
    "app-quotes": QuoteGrid,
    "app-new-quote": NewQuote
  }
};
</script>

<style>
</style>
