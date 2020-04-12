<template>
  <div class="container">
    <app-header :quoteCount="quotes.length" :maxQuotes="maxQuotes"></app-header>
    <app-new-quote @quoteAdded="newQuote"></app-new-quote>
    <app-quotes :quotes="quotes"></app-quotes>
    <div class="row">
      <div class="col-sm-12 text-center">
        <div class="alert alert-info">Info: Click on the quote to delete it!</div>
      </div>
    </div>
  </div>
</template>

<script>
import Header from "./components/Header.vue";
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
    "app-header": Header,
    "app-quotes": QuoteGrid,
    "app-new-quote": NewQuote
  },
  methods: {
    newQuote(quote) {
      if (this.quotes.length >= this.maxQuotes) {
        return alert(
          "You reached your maximum number of quotes. You have to delete a quote first"
        );
      }
      this.quotes.push(quote);
    }
  }
};
</script>

<style>
</style>
