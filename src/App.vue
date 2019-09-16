<template>
  <div id="app" class="container">
    <NewQuote @quoteAdded="emitQuote"></NewQuote>
    <QuoteGrid :quotes="quotes"></QuoteGrid>
    <div class="row">
      <div class="col-sm-12 text-center">
        <div class="alert alert-info" style="margin: 10px 0;">
          <p>Info: Click on a Quote to delete it!</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import QuoteGrid from './components/QuoteGrid'
import NewQuote from './components/NewQuote'

export default {
  components: {
    QuoteGrid,
    NewQuote
  },
  data () {
    return {
      quotes: ['Just a Quote to see something'],
      maxQuotes: 10
    }
  },
  methods: {
    emitQuote (data) {
      this.quotes.push(data)
    }
  }
}
</script>

<style>

</style>
