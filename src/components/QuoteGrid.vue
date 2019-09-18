<template>
  <!-- eslint-disable -->
  <div class="row">
    <Quote v-for="(quote, index) in quotes" :key="index" @click.native="deleteQuote(index)">
      {{quote}}
    </Quote>
  </div>
</template>

<script>
import Quote from './Quote'

export default {
  components: {
    Quote
  },
  props: ['quotes'],
  methods: {
    deleteQuote (index) {
      this.$emit('quoteDeleted', index)
    }
  }
}
</script>

<style>

</style>
