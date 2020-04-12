<template>
  <div class="container">
    <app-header></app-header>
    <app-new-quote @quoteAdded="quotes.push($event)"></app-new-quote>
    <app-quotes :quotes="quotes"></app-quotes>
    <div class="row">
      <div class="col-sm-12 text-center">
        <div class="alert alert-info">Info: Click on the quote to delete it!</div>
      </div>
    </div>
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
