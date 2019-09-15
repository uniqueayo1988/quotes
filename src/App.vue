<template>
  <div id="app" class="container">
    <QuoteGrid :quotes="quotes"></QuoteGrid>
  </div>
</template>

<script>
import QuoteGrid from './components/QuoteGrid'

export default {
  components: {
    QuoteGrid
  },
  data () {
    return {
      quotes: ['Just a Quote to see something'],
      maxQuotes: 10
    }
  }
}
</script>

<style>

</style>
