<template>
  <div id="app">
    <quote-head :quoteCount="quoteCount" :maxQuotes="maxQuotes"></quote-head>
    <quote-input :addQuote="addQuote"></quote-input>
    <quotes-display :quotes="quotes"></quotes-display>
  </div>
</template>

<script>
import QuoteHead from './components/QuoteHead';
import QuoteInput from './components/QuoteInput';
import QuotesDisplay from './components/QuotesDisplay';

export default {
  name: 'app',
  data: function() {
    return {
      quoteCount: 0,
      maxQuotes: 10,
      quotes: [],
    };
  },
  methods: {
    addQuote(newQuote) {
      this.quoteCount += 1;
      this.quotes.push(newQuote);
    },
  },
  components: {
    QuoteHead,
    QuoteInput,
    QuotesDisplay,
  },
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
  width: 100%;
  height: 100%;
  overflow: hidden;
}
</style>
