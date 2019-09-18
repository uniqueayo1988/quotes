<template>
  <div id="app" class="container">
    <Header :quoteCount="quotes.length" :maxQuotes="maxQuotes"></Header>
    <NewQuote @quoteAdded="emitQuote"></NewQuote>
    <QuoteGrid :quotes="quotes" @quoteDeleted="deleteQuote"></QuoteGrid>
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
import Header from './components/Header'

export default {
  components: {
    QuoteGrid,
    NewQuote,
    Header
  },
  data () {
    return {
      quotes: ['Just a Quote to see something'],
      maxQuotes: 10
    }
  },
  methods: {
    emitQuote (data) {
      if (this.quotes.length >= this.maxQuotes) {
        return alert('Please delete Quotes first!')
      }
      this.quotes.push(data)
    },
    deleteQuote (index) {
      this.quotes.splice(index, 1)
    }
  }
}
</script>

<style>

</style>
