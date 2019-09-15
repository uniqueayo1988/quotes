<template>
  <!-- eslint-disable -->
  <div class="row">
    <Quote v-for="(quote, i) in quotes" key="i">
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
  data () {
    return {
    }
  }
}
</script>

<style>

</style>
