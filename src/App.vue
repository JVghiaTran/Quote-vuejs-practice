<template>
  <div class="container">
    <new-quote @quoteAdded="NewQuote"></new-quote>
    <quote-grid :quotesss="quotes" @quoteDel="deleteQuote"></quote-grid>
    <div class="row text-center">
      <div class="col-sm-6">
        <div class="alert alert-info">Click on quote to delete!</div>
      </div>
    </div>
  </div>
</template>

<script>
import QuoteGrid from './components/QuoteGrid'
import NewQuote from './components/NewQuote'

export default {
  data: function() {
    return {
      quotes: ['asd'],
      maxQuotes: 10
    }
  },
  methods: {
    NewQuote(quote) {
      this.quotes.push(quote)
    },
    deleteQuote(index) {
      this.quotes.splice(index, 1)
    }
  },
  components: {
    QuoteGrid,
    NewQuote
  }
}
</script>

<style scoped>

</style>
